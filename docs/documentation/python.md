# Python

## 1. Python Syntax

### Print Statement
A `print` statement is the easiest way to get your Python programme to communicate with you.

There are two different Python versions. Both Python 2 and Python 3 are used throughout the globe. The most significant difference between the two is how you write a `print` statement. In Python 3, `print` has parentheses.

``` python
print("Hello World!")
```

### Strings

Text in Python is considered a specific type of data called a string. A string, so named because they’re a series of letters, numbers, or symbols connected in order — as if threaded together by *string*. Strings can be defined in different ways:

```print "This is a good string"```
```print 'You can use single quotes for a string as well'```

Double-quotes (“) and single-quotes (‘) are both acceptable ways to define a string.

We can combine multiple strings using +, like so:

```print "This is " + "a good string"````

### Variables

Python uses variables to define things that are subject to change.

```greeting_message = "Welcome to Codecademy!"```
```current_excercise = 5```

Variables = Values assigned subject to changed 

#### Updating Variables

Changing the contents of a variable is one of the essential operations. As the flow of a programme progresses, data should be updated to reflect changes that have happened.

``` python
fish_in_clarks_pond = 50

print "Catching fish"

number_of_fish_caught = 10
fish_in_clarks_pond = fish_in_clarks_pond - number_of_fish_caught
```
#### Numbers

Variables can also hold numeric values. The simplest kind of number in Python is the integer, which is a whole number with no decimal point:

```python
int = 1
```

A number with a decimal point is called a *float*. You can define floats with numbers after the decimal point or by just including a decimal point at the end:

``` python
float = 1.0
float = 1.
```

#### Booleans

Sometimes we have a need for variables that are either true or false. This datatype, which can only ever take one of two values, is called a `boolean`. In Python, we define booleans using the keywords True and False:

``` python
a = True
b = False
```

A boolean is actually a special case of an integer. A value of `True` corresponds to an integer value of `1`, and will behave the same. A value of `False` corresponds to an integer value of `0`.

#### ValueError

Python automatically assigns a variable the appropriate datatype based on the value it is given. 
A variable with the value 7 is an integer, 7. is a float, "7" is a string. 

Sometimes we will want to convert variables to different datatypes. For example, if we wanted to print out an integer as part of a string, we would want to convert that integer to a string first. 

We can do that using str():

``` python
age = 13
print "I am " + str(age) + " years old!"
This would print:

>>> "I am 13 years old!"
```

## 2. Strings

Another useful data type is the string. A string can contain letters, numbers, and symbols.

``` python
name = "Ryan"
age = "19"
food = "cheese"
```

### Access by Index

Each character in a string is assigned a number. This number is called the index. Check out the diagram in the editor.

``` python
c = "cats"[0]
n = "Ryan"[3]
```

### String Methods

Now that we know how to store strings, let’s see how we can change them using string methods.

String methods let you perform specific tasks for strings.

We’ll focus on four string methods:

``` python
len()
lower()
upper()
str()
```
#### len()

Let’s start with `len()`, which gets the length (the number of characters) of a string!

Create a variable and set it to a string. The output will be the number of characters.

```python
parrot = "Norwegian Blue"
print len(parrot)
```
#### low()

You can use the `lower()` method to get rid of all the capitalization in your strings. You call `lower()` like so:

```python
"Ryan".lower()
```

#### upper()

A similar method exists to make a string completely `upper` case.

```python
"ryan".upper()
```

#### str()

Now let’s look at `str()`, which is a little less straightforward. The `str()` method turns non-strings into strings! For example:

``` python
str(2)
```

would turn 2 into "2".

### Dot Notation

Let’s take a closer look at why you use `len(string)` and `str(object)`, but dot notation (such as `"String".upper()`) for the rest.

``` python
lion = "roar"
len(lion)
lion.upper()
```

Methods that use dot notation only work with strings.

On the other hand, `len()` and `str()` can work on other data types.

### Explicit String Conversion

Sometimes you need to combine a string with something that isn’t a string. In order to do that, you have to convert the non-string into a string.

```python
print "I have " + str(2) + " coconuts!"
```

The `str()` method converts non-strings into strings. In the above example, you convert the number `2` into a string and then you concatenate the strings together just like in the previous exercise.

### String Formatting with % 

When you want to print a variable with a string, there is a better method than concatenating strings together.

``` python
name = "Mike"
print "Hello %s" % (name) 
```

The `%` operator after the string is used to combine a string with variables. The `%` operator will replace the `%s` in the string with the string variable that comes after it.

Remember, we use the `%`operator to replace the `%s` placeholders with the variables in parentheses.

## 3. Conditionals and Control Flow

Let’s start with the simplest aspect of control flow: comparators. There are six:

`Equal to (==)`

``` python
>>> 2 == 2
True
>>> 2 == 5
False
```

`Not equal to (!=)`

``` python
>>> 2 != 5
True
>>> 2 != 2
False
```

Comparators check if a value is (or is not) equal to, greater than (or equal to), or less than (or equal to) another value.

Note that `==` compares whether two things are equal, and `=` assigns a value to a variable.

### Boolean Operators

Boolean operators compare statements and result in boolean values. There are three boolean operators:

`and`, which checks if both the statements are `True`;
`or`, which checks if at least one of the statements is `True`;
`not`, which gives the opposite of the statement.
We’ll go through the operators one by one.

Boolean operators aren’t just evaluated from left to right. Just like with arithmetic operators, there’s an order of operations for boolean operators:

`not` is evaluated first;
`and` is evaluated next;
`or` is evaluated last.

### Conditional Statement Syntax

`if` is a conditional statement that executes some specified code after checking if its expression is `True`.

Here’s an example of `if` statement syntax:

``` python
if 8 < 9:
  print "Eight is less than nine!"
```

The `else` statement complements the `if` statement. An `if/else` pair says: “If this expression is true, run this indented code block; otherwise, run this code after the else statement.”

Unlike `if`, `else` doesn’t depend on an expression. For example:

``` python
if 8 > 9:
  print "I don't get printed!"
else:
  print "I get printed!"
```

`elif` is short for “else if.” It means exactly what it sounds like: “otherwise, if the following expression is true, do this!”

``` python
if 8 > 9:
  print "I don't get printed!"
elif 8 < 9:
  print "I get printed!"
else:
  print "I also don't get printed!"
```

In the example above, the `elif` statement is only checked `if` the original if statement is `False`.

## 4. Functions

Functions are defined with three components:

The *header*, which includes the def keyword, the name of the function, and any parameters the function requires. Here’s an example:

``` python 
def hello_world(): # There are no parameters
```

An optional *comment* that explains what the function does.

```python
"""Prints 'Hello World!' to the console."""
```

The *body*, which describes the procedures the function carries out. The body is indented, just like conditional statements.

```python
print "Hello World!"
```

Here’s the full function pieced together:

``` python
def hello_world():
  """Prints 'Hello World!' to the console."""
  print "Hello World!"
```

### Paramters and Arguments 

Let’s take another look at the definition of the function square from the previous exercise:

``` python
def square(n):
```

Here, `n` is a parameter of `square`. A parameter is a variable that is an input to a function. It says, “Later, when `square` is used, you’ll be able to input any value you want, but for now we’ll call that future value n.” A function can have any number of parameters.

The values of the parameters passed into a function are known as the arguments. 

Typically, when you call a function, you should pass in the same number of arguments as there are parameters.

To summarize:

- When defining a function, placeholder variables are called parameters.
- When using, or calling, a function, inputs into the function are called arguments.

### Function Calling Functions 

We’ve seen functions that can print text or do simple arithmetic, but functions can be much more powerful than that. For example, a function can call another function:

```python
def fun_one(n):
  return n * 5

def fun_two(m):
  return fun_one(m) + 7
```

### Generic Imports

When you simply import a module this way, it’s called a generic import. There are Python modules  that include a number of useful variables and functions.

```python
import math
print math.sqrt(25)
```
### Function Imports

It’s possible to import only certain variables or functions from a given module. 
Pulling in just a single function from a module is called a function import, and it’s done with the `from` keyword:

```python
from module import function
```

### max()

The `max()` function takes any number of arguments and returns the largest one. (“Largest” can have odd definitions here, so it’s best to use `max()` on integers and floats, where the results are straightforward, and not on other objects, like strings.)

### min()

`min()` then returns the smallest of a given series of arguments.

### abs()

The `abs()` function returns the absolute value of the number it takes as an argument—that is, that number’s distance from `0` on an imagined number line. For instance, `3` and `-3` both have the same absolute value: `3`. The `abs()` function always returns a positive value, and unlike `max()` and `min()`, it only takes a single number.

### type()

Finally, the `type()` function returns the type of the data it receives as an argument. If you ask Python to do the following:

```python
print type(42)
print type('spam')
```

Python will output:

```python
<type 'int'>
<type 'float'>
<type 'str'>
```

## 5. Lists & Dictionaries

#### Introduction to Lists

Lists are a *datatype* you can use to store a collection of different pieces of information as a sequence under a single variable name. (Datatypes you’ve already learned about include strings, numbers, and booleans.)

You can assign items to a list with an expression of the form.

``` python
list_name = [item_1, item_2]
```

with the items in between brackets. A list can also be empty: ```empty_list = []```.

Lists are very similar to strings, but there are a few key differences.

#### Access by Index




## 6. Loops

[Python Standard Library](https://docs.python.org/3/library/index.html#library-index)

## Compound Statement

- [The if Statement](https://docs.python.org/3/reference/compound_stmts.html#the-if-statement)
- [The while Statement](https://docs.python.org/3/reference/compound_stmts.html#the-while-statement)
- [The for Statement](https://docs.python.org/3/reference/compound_stmts.html#the-for-statement)
- [The try Statement](https://docs.python.org/3/reference/compound_stmts.html#the-try-statement)

