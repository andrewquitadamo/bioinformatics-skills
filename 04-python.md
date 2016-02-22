#Python

Python is a programming language commonly used in bioinformatics

While its syntax is simpler than other programming languages it is quite powerful

In our lab we use Python for parsing files, and other tasks that are too complicated to be done with the command line.

#Very Basic Python

To get started with Python, we'll use the interactive shell. 

To open it, simply type `python`

You should see some information about your Python install, and a prompt that looks like `>>>`

#Expressions

Expression can be evaluated on the Python shell like `2+2` or `'hello' + ' world'` or `max([1,2,4])`

**Instructions* 
Try inputting a few of the above expressions.  
Try inputting a few of your own, and see what happens.

#Types

Values in Python are assigned to a type.

Types allow Python to know what operations are allowed, and how to behave.

For example `+` on Ints, Floats, or Longs (number types) acts as addition. 

On Strings `+` acts as concatenation. 

You can check the type of a value or expression by using the `type()` function, like `type(3)`

You can convert between types using functions like `int()`, `float()` or `str()`

**Instructions* 
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

**Instructions* 
Create a few variables of your own. They don't have to be numbers.  
Try creating a variable to store your first name.  

#Strings

Strings are used to store text. They have a few special methods associated with them.  
`name = "Andrew"`

We can use the len() function to find the length of a string.  
`len(name)`

We can combine strings using the `+`. This is called concatenation.  
`name + " Q."`  

We can use string methods, like .lower(), upper(),split() on strings.  
`name.lower()`  
`header="gene\tchr\tpos"`  
`header.split("\t")`

#Lists

Lists are another data type that you will use a lot. They store values in an ordered data structure.  
`a = [0,1,3]`  
`b = ['Loxodonta africana','Rattus norvegicus']`  

We can access any element in a list by using subsetting. Remember Python starts counting at 0.  
`b[0]`

Just like strings, lists have special methods too. These include .index(), .append(), and .pop()  
`b.append('Macropus eugenii')`  
`b`

#Functions

Functions are reusable bits of code. Python already has built-in functions, and we can write our own.

Two examples of built-in Python functions are abs() and max().  
`abs(-14)`  
`max([1,2,4])`

The syntax to call a function is the function name, followed by parentheses, and then the values we want to pass to the function.
Python then evaluates the function with the given inputs, and returns a value.

We can write our own functions too. The general syntax is 
```
def function_name(inputs):
		things_to_do
		return result
```

#Functions (cont.)

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

**Instructions* 
Modify the example functions in some way.  
You could change the square function to take two inputs, a base and a power, and return the result of base^power.  
You could change the greeting function so that it takes a first and last name.

#For Loops

For loops can be used to iterate over lists, or to do things multiple times.
Example:
```
numbers=[0,1,2,3,4,5]
for number in numbers:
		print number*2
```

The `for...in...` syntax is very useful in iterating over lists.

You can also nest for loops
```
numbers=[0,1,2,3,4,5]
for number in numbers:
		for number2 in numbers:
			print number*number2
```

#Conditionals (if, elif, else)

Statements like these return a boolean (True or False)  
`0>5`  
`"name"=="name"`  

We can use conditionals to perform actions based on the statements value.
```
if 0>5:
		print "Not good"
else:
		print "Everything is alright"
```

if checks for truth, else catches anything that is false.  
elif can be used to check for truth again. It is short for else-if.
```
species='Loxodonta africana'
if species == 'Homo sapiens':
		print "Human"
elif species == 'Loxodonta africana':
		print "African elephant"
else:
		print "Unknown"
```
