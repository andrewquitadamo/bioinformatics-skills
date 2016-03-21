class: center, middle

#Python Part 2

---

#Python Continued

We previously covered some of the basic principles of Python.

--

In this lesson we will talk about a few more topics and discuss how to create a Python script.

---

# Dictionaries

Dictionaries provide a one-to-one mapping from key to value. 

--

They allow you to store and then access values based on their key.

```
fruit = {'orange': 1, 'apples':2}
fruit['orange']
```

--

This is useful for storing values based on a unique ID, such as gene name, or rsID.

You can also create and fill a dictionary dynamically:
```
Dict = {}
Dict['first_name']='Edward'
Dict['last_name']='Jennar'
```

--

You can update the values in the dictionary:
```
Dict['last_name']='Jenner'
```

---

# Dictonaries (cont.)

You can create nested dictionaries:
```
english_scientists = {'JennerE':{'first_name': 'Edward', 'last_name': 'Jenner', 'birth_year': 1749},
					  'SnowJ':{'first_name': 'John', 'last_name': 'Snow', 'birth_year': 1813}}
```

--

**Instructions**  
Using the dictionary examples try to add new values and update values.  
Try to access the `first_name` value of `JennerE` in the `english_scientists` dictionary.

---

# Files

One of the most common things you will do in bioinformatics is open a file to read data from it.

--

One of the ways you can do this is by using this syntax:
```
with open(filename, 'r') as file:
    for line in file:
        print(line)
```

--

Using the `with open` and `for line in` syntax allows you to read one line at a time, which makes it good for processing large files.

--

**Instructions**  
Using the syntax above attempt to open up a file and print out its contents.

---

# Printing

There is a difference between how printing works in Python 2 vs Python 3

--

You can use Python 3 syntax in Python 2 by importing it from the future.

```
from __future__ import print_function
```

--

The print function has certain capabilities that the print statement from Python 2 doesn't.

```
print('hello','world',sep='\t')
```

--

The print function also has a file argument, so you can specify where to print to. You can even print to the stderr.

--

**Instructions**  
Import the print function and play around with it. Try the sep argument. See what happens when you use `end=''`.

---

#Python Scripts

So far we've been using the interactive shell to play around with Python. But in reality most of your work will involve creating and running scripts.

--

So instead of typing in what you want to the shell, you put your Python code into a text file, save it, and then run it.

--

**Instructions**  
Create a file called `hello.py`.
In the file import the print function, and then use it to print out a greeting.

