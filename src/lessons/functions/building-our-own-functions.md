# Building our own functions

<aside>

🧑🏿‍🍳 A function is like a recipe. It has ingredients, steps to follow, and if all goes to plan, there’s a ‘meal’ that it produces. So far, your programs have used recipes from Python’s “recipe book” — built-in functions. Now, you’ll see how to write your own recipes, and tell Python to follow them step by step.

</aside>

## Video: Functions in Python

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/584390ac33ac47e096bc92d693a84cc0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

### Defining a function

We use the keyword `def` (short for ‘define’) to create a new function. When you define a function, you specify a *name* for the function as well as a sequence of statements in an indented block. The function is stored in the program’s memory, but the code does not run right away. After the definition, we can *call* the function to run the code.

Here’s what it looks like:

```python
# Define a function.
def function_name(parameter_1, parameter_2):
	# Follow these steps (the indented function body)
	# print each parameter
	print(parameter_1)
	print(parameter_2)

# Use function_name to call the function.
function_name(argument_1, argument_2)
```

When defining a function:

- Use the keyword `def`
- Give the function a name, ideally one that tells what the function does
- Give names for each of the function's parameters
- Use an indented block for the code for the function

Below is an example of a Python function that calculates the sum of two numbers:

```python
def add(a, b):
  return a + b
```

Later, when we want to run the statements in the function, we call the function, which runs the code from the function definition.

```python
add(3, 5) # 8
add(10, 30) # 40
```

## Parameters and Arguments

```python
def add(a, b):
  return a + b
```

In the example above, `a` and `b` are **parameters**. Parameters are names that stand in for the values passed to the function. You use them in the function body like variables.

We can call the add function like this:

```python
>>> add(3,5)
8
```

The values passed to the function are called **arguments**. In this example, `3` and `5` are arguments. The parameters `a` and `b` get assigned the values `3` and `5` in the function body.

<aside>


🤷🏿‍♂️ An **argument** is a value provided to a function when the function is called.
A **parameter** is a named spot in a function definition, where the argument will go.

Parameters **and arguments **are similar concepts. Parameters are in the definition, arguments are when you actually call the function. It’s not super important that you memorize which is which. A lot of programmers use the terms interchangeably.

</aside>

## Practice

<aside>


👩🏿‍💻 Write a function called **greet** which will print out three lines of personalized greeting. The function should take as its argument a name then print the messages below. Modify the starter code below.

</aside>

A sample run of your code with argument Keno, i.e., `greet("Keno")` should look like this:

![sample run of greet person function](./building-our-own-functions/greet-keno-result.png)

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/Greet-Person-Function" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

<aside>


🤔 Modify the code above to put the function definition at the end of the program. What do you notice happens? Try it first then click below for the explanation.

- Explanation

    If you put the function definition at the end of the program, you will get an error. A function must be defined before you use it in your program. If you write greet(Keno) first, Python doesn't know this function and will error. We must define functions at the beginning of our programs before we use them. **There is a way however to get around this (call a function that its definition comes later in the file) but it is out of our discussion scope now)**.

</aside>
j
## Functions can have any code inside

Any code can go inside a function. Variables, loops, conditions, other function calls — it all works. Anything that you’ve written in a program so far can go inside a function.

```python
# A function with an if/else statement
def check_password(attempt):
	password = "sEcRetPaSsWoRd"
	if attempt = password:
		return "You're in!"
	else:
		return "Access denied"

print(check_password("open sesame")) # Access denied
print(check_password("sEcRetPaSsWoRd")) # You're in!

# A function with a loop inside
def add_up_to(number):
	total = 0
	for i in range(1,number):
		total += number
	return total

print(add_up_to(5))   # 20
print(add_up_to(10))  # 90
print(add_up_to(100)) # 9900
```

<aside>


⚠️ **Indentation**
Make sure you get the indentation right. Indent one more level for each block some code is inside of. So, if some code is inside a condition, and the conditional is inside a function, the code in the conditional is indented 2 times.

```python
# Showing the indentation with ->
def check_password(attempt):
->password = "sEcRetPaSsWoRd"
->if attempt = password:
->->return "You're in!"
```

</aside>