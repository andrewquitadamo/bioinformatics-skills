#Python

Python is a programming langauge commonly used in bioinformatics

While its syntax is simpler than other programming languages it is quite powerful

In our lab we use Python for parsing files, and other tasks that are too complicated to be done with the command line.

#Very Basic Python

To get started with Python, we'll use the interactive shell. 

To open it, simply type `python`

You should see some information about your Python install, and a prompt that looks like `>>>`

#Expressions

Expression can be evaluated on the Python shell like `2+2` or `'hello' + ' world'` or `max([1,2,4])`

**Instructions**  
Try inputting a few of the above expressions.  
Try inputting a few of your own, and see what happens.

#Types

Values in Python are assigned to a type.

Types allow Python to know what opperations are allowed, and how to behave.

For example `+` on Ints, Floats, or Longs (number types) acts as addition. 
On Strings `+` acts as concatonation. 

You can check the type of a value or expression by using the `type()` function, like `type(3)`

You can convert between types using functions like `int()`, `float()` or `str()`

**Instructions**  
Check the types of a few of the expressions you previously used  
Try converting `3` to a float, and try converting `3` to a string  

#Variables

Variables allow you to store values.  
Variables also have types, ranging from the simple (Ints, Floats, and Strings) to the more complex (Lists and Dictionaries).

You assign a value to a variable by using the equals sign. 
`age = 25`

We can now use this variable in expressions.
`age - 10`

We can also update the variable
`age += 1`

The `+=` syntax is equivalent to `age = age + 1`

**Instructions**  
Create a few variables of your own. They don't have to be numbers.  
Try creating a variable to store your first name.  

#Functions

Functions are reusable bits of code. Python already has built-in functions, and we can write our own.

Two examples of built-in Python functions are abs() and max().  
`abs(-14)`  
`max([1,2,4])`

The syntax to call a function is the function name, followed by paranthases, and then the values we want to pass to the function.
Python then evaluates the function with the given inputs, and returns a value.

We can write our own functions too. The general syntax is 
```
def function_name(inputs):
	things_to_do
	return result
```

So if we wanted to create a function that squared numbers it would look like:
```
def square(x):
	return x**2
```

Or if we wanted to create a function that takes a persons name, and returns a greeting we could create a function like:
```
def say_hello(name):
	greeting = "Hello " + name
	return greeting
```

**Instruction**
Modify the example functions in some way.  
You could change the square function to take two inputs, a base and a power, and return the result of bash^power.
You could change the greeting function so that it takes a first and last name.
