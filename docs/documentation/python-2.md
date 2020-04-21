# Python 2

## 1. Python Syntax

### Print Statement
A `print` statement is the easiest way to get your Python programme to communicate with you.

There are two different Python versions. Both Python 2 and Python 3 are used throughout the globe. The most significant difference between the two is how you write a `print` statement. In Python 3, `print` has parentheses.

``` python
print("Hello World!")
```

### Strings

Text in Python is considered a specific type of data called a string. A string, so named because they’re a series of letters, numbers, or symbols connected in order — as if threaded together by *string*. Strings can be defined in different ways:

``` python 
print "This is a good string"
```

``` python 
print 'You can use single quotes for a string as well'
```

Double-quotes (“) and single-quotes (‘) are both acceptable ways to define a string.

We can combine multiple strings using +, like so:

``` python
print "This is " + "a good string"````

### Variables

Python uses variables to define things that are subject to change.

``` python
greeting_message = "Welcome to Codecademy!"
```

``` python
current_excercise = 5
```
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

#### max()

The `max()` function takes any number of arguments and returns the largest one. (“Largest” can have odd definitions here, so it’s best to use `max()` on integers and floats, where the results are straightforward, and not on other objects, like strings.)

#### min()

`min()` then returns the smallest of a given series of arguments.

#### abs()

The `abs()` function returns the absolute value of the number it takes as an argument—that is, that number’s distance from `0` on an imagined number line. For instance, `3` and `-3` both have the same absolute value: `3`. The `abs()` function always returns a positive value, and unlike `max()` and `min()`, it only takes a single number.

#### type()

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

### Introduction to Lists

Lists are a *datatype* you can use to store a collection of different pieces of information as a sequence under a single variable name. (Datatypes you’ve already learned about include strings, numbers, and booleans.)

You can assign items to a list with an expression of the form.

``` python
list_name = [item_1, item_2]
```

with the items in between brackets. A list can also be empty: ```empty_list = []```.

Lists are very similar to strings, but there are a few key differences.

### Access by Index

You can access an individual item on the list by its index. An index is like an address that identifies the item’s place in the list. The index appears directly after the list name, in between brackets, like this: `list_name[index]`.

List indices begin with 0, not 1! You access the first item in a list like this: `list_name[0]`. The second item in a list is at index 1: `list_name[1]`. 

### List Index

A list index behaves like any other variable name! It can be used to access as well as assign values.

You saw how to access a list index like this:

``` python
zoo_animals[0]
# Gets the value "pangolin"
```

You can see how assignment works on line 5:

```python
zoo_animals[2] = "hyena"
# Changes "sloth" to "hyena"
```

#### Lenght of a List Index

A list doesn’t have to have a fixed length. You can add items to the end of a list any time you like!

```python
letters = ['a', 'b', 'c']
letters.append('d')
print len(letters)
print letters
```

### List Slicing

Sometimes, you only want to access a portion of a list. Consider the following code:

``` python
letters = ['a', 'b', 'c', 'd', 'e']
slice = letters[1:3]
print slice
print letters
```

What is this code doing?

First, we create a list called `letters`.

Then, we take a subsection of the list and store it in the `slice` list. We do this by defining the indices we want to include after the name of the list: `letters[1:3]`. 

In Python, when we specify a portion of a list in this manner, we **include** the element with the first index, `1`, but we **exclude** the element with the second index, `3`.

Next, we print out `slice`, which will print `['b','c']`. Remember, in Python indices always start at 0, so the 1 element is actually `b`.

Finally, we print out `['a', 'b', 'c', 'd', 'e']`, notice that we did not modify the original `letters` list.

#### Slicing Lists & Strings

You can slice a string exactly like a list! In fact, you can think of strings as lists of characters: each character is a sequential item in the list, starting from index 0.

```python
my_list[:2]
# Grabs the first two items
my_list[3:]
# Grabs the fourth through last items
```

If your list slice includes the very first or last item in a list (or a string), the index for that item doesn’t have to be included.

#### Use For Loop to Access Lists

If you want to do something with every item in the list, you can use a for loop. 

```python
for variable in list_name:
  # Do stuff!
```

A variable name follows the `for` keyword; it will be assigned the value of each list item in turn.

Then `in list_name` designates `list_name` as the list the loop will work on. The line ends with a colon (`:`) and the indented code that follows it will be executed once per item in the list.

#### Use For Loop to Sort Lists

If your list is a jumbled mess, you may need to `sort()` it.

```python
animals = ["cat", "ant", "bat"]
animals.sort()

for animal in animals:
  print animal
```

First, we create a list called `animals` with three strings. The strings are not in alphabetical order.

Then, we sort `animals` into alphabetical order. Note that `.sort()` modifies the list rather than returning a new list.

Then, for each item in `animals`, we print that item out as `"ant"`, `"bat"`, `"cat"` on their own line each.


### Dictionaries

A dictionary is similar to a list, **but you access values by looking up a *key* instead of an index**. A key can be any string or number. Dictionaries are enclosed in curly braces, like so:

```python
d = {'key1' : 1, 'key2' : 2, 'key3' : 3}
```

This is a dictionary called `d` with three *key-value pairs.* The key `'key1'` points to the value `1`, `'key2'` to `2`, and so on.

Dictionaries are great for things like phone books (pairing a name with a phone number), login pages (pairing an e-mail address with a username), and more!

#### New Entries for Dictionaries

Like Lists, Dictionaries are *mutable*. This means they can be changed after they are created. One advantage of this is that we can add new *key/value pairs* to the dictionary after it is created like so:

```python
dict_name[new_key] = new_value
```

An empty pair of curly braces `{}` is an empty dictionary, just like an empty pair of `[]` is an empty list.

The length `len()` of a dictionary is the number of key-value pairs it has. Each pair counts only once, even if the value is a list. (That’s right: you can put lists *inside* dictionaries!)

#### Changes and Deletions in Dictionaries

Because dictionaries are mutable, they can be changed in many ways. Items can be removed from a dictionary with the `del` command:

```python
del dict_name[key_name]
```

will remove the key `key_name` and its associated value from the dictionary.

A new value can be associated with a key by assigning a value to the key, like so:

``` python
dict_name[key] = new_value
```

#### Removals in Lists 

Sometimes you need to remove something from a list.

``` python
beatles = ["john","paul","george","ringo","stuart"]
beatles.remove("stuart")
print beatles
```

This code will print:

``` python
 ["john","paul","george","ringo"]
```

We create a list called `beatles` with 5 strings.

Then, we remove the first item from `beatles` that matches the string `"stuart"`. Note that .remove(item) does not return anything.

Finally, we print out that list just to see that `"stuart"` was actually removed.

#### Notes about Dictionaries

Let’s go over a few last notes about dictionaries

 ```python
my_dict = {
  "fish": ["c", "a", "r", "p"],
  "cash": -4483,
  "luck": "good"
}
print my_dict["fish"][0]
```

In the example above, we created a dictionary that holds many types of values.

The key `"fish"` has a list, the key `"cash"` has an int, and the key `"luck"` has a string.

Finally, we print the letter `"c"`. When we access a value in the dictionary like `my_dict["fish"]`, we have direct access to that value (which happens to be a list). We can access the item at index `0` in the list stored by the key `"fish"`.

## 6. Lists and Functions

Now that you’ve learned about lists, let’s turbo-charge them with functions.

### Removing Elements from Lists

You have a few options. For a list called `n`:

`n.pop(index)` will remove the item at `index` from the list and return it to you:

```python
n = [1, 3, 5]
n.pop(1)
# Returns 3 (the item at index 1)
print n
# prints [1, 5]
```

`n.remove(item)` will remove the actual `item\ if it finds it:

``` python
n.remove(1)
# Removes 1 from the list,
# NOT the item at index 1
print n
# prints [3, 5]
```

`del(n[1])` is like `.pop` in that it will remove the item at the given index, but it won’t return it:

``` python
del(n[1])
# Doesn't return anything
print n
# prints [1, 5]
```

### Passing a List to a Function

You pass a list to a function the same way you pass any other argument to a function.

```python
def list_function(x):
    return x

n = [3, 5, 7]
print list_function(n)
```

### Using an Element from a List in a Function

Passing a list to a function will store it in the argument (just like with a string or a number!)

```python
def first_item(items):
  print items[0]

numbers = [2, 7, 9]
first_item(numbers)
```

In the example above, we define a function called `first_item`. It has one argument called `items`.

Inside the function, we `print` out the item stored at index zero of `items`.

After the function, we create a new list called `numbers`.

Finally, we call the `first_item` function with numbers as its argument, which prints out `2`.

### Modifying an Element of a List in a Function 

Modifying an element in a list in a function is the same as if you were just modifying an element of a list outside a function.

``` python
def double_first(n):
  n[0] = n[0] * 2

numbers = [1, 2, 3, 4]
double_first(numbers)
print numbers
```

We create a list called `numbers`.

We use the `double_first` function to modify that list.

Finally, we print out `[2, 2, 3, 4]`

When we pass a list to a function and modify that list, like in the `double_first` function above, we end up modifying the original list.

### List Manipulation in Functions

You can also append or delete items of a list inside a function just as if you were manipulating the list outside a function.

``` python
my_list = [1, 2, 3]
my_list.append(4)
print my_list
# prints [1, 2, 3, 4]
```

The example above is just a reminder of how to append items to a list.

### Passing a Range into a Function

The Python `range()` function is just a shortcut for generating a list, so you can use ranges in all the same places you can use lists.

``` python
range(6) # => [0, 1, 2, 3, 4, 5]
range(1, 6) # => [1, 2, 3, 4, 5]
range(1, 6, 3) # => [1, 4]
```

The `range` function has three different versions:

`range(stop)`
`range(start, stop)`
`range(start, stop, step)`

In all cases, the `range()` function returns a list of numbers from `start` up to (but not including) `stop`. Each item increases by step.

If omitted, `start` defaults to `0` and `step` defaults to `1`.

### Iterating over a List in a Function

Now that we’ve learned about `range`, we have two ways of iterating through a list.

Method 1 - `for item in list`:

``` python
for item in list:
  print item
```

Method 2 - iterate through indexes:

``` python
for i in range(len(list)):
  print list[i]
``` 

Method 1 is useful to loop through the list, but it’s not possible to modify the list this way.

Method 2 uses indexes to loop through the list, making it possible to also modify the list if needed. Since we aren’t modifying the list, feel free to use either one on this lesson!

### Using Strings in Lists in Functions

Now let’s try working with strings!

``` python
for item in list:
  print item

for i in range(len(list)):
  print list[i]
```
  
The example above is just a reminder of the two methods for iterating over a list.

### Using Two Lists as Two Arguments in a Function

Using multiple lists in a function is no different from just using multiple arguments in a function!

``` python
a = [1, 2, 3]
b = [4, 5, 6]
print a + b
# prints [1, 2, 3, 4, 5, 6]
```

The example above is just a reminder of how to concatenate two lists.

### Using a List of Lists in a Function

Using multiple lists in a function is no different from just using multiple arguments in a function!

```python
a = [1, 2, 3]
b = [4, 5, 6]
print a + b
# prints [1, 2, 3, 4, 5, 6]
```

The example above is just a reminder of how to concatenate two lists.

## 7. Loops

### While Loop

The `while` loop is similar to an `if` statement: it executes the code inside of it if some condition is true. The difference is that the `while` loop will continue to execute as long as the condition is true. In other words, instead of executing if something is true, it executes while that thing is true.

### Condition

The condition is the expression that decides whether the loop is going to continue being executed or not. There are 5 steps to this program:

The `loop_condition`variable is set to `True`

The `while` loop checks to see if `loop_condition` is `True`. It is, so the loop is entered.

The `print` statement is executed.

The variable `loop_condition` is set to False.

The `while` loop again checks to see if `loop_condition` is `True`. It is not, so the loop is not executed a second time.

``` python
loop_condition = True

while loop_condition:
  print "I am a loop"
  loop_condition = False
```

### Infinite Loops

An *infinite* loop is a loop that never exits. This can happen for a few reasons:

The loop condition cannot possibly be false (e.g. `while 1 != 2`)

The logic of the loop prevents the loop condition from becoming false.

Example:

``` python
count = 10
while count > 0:
  count += 1 # Instead of count -= 1
```

### Break

The `break` is a one-line statement that means “exit the current loop.” An alternate way to make our counting loop exit and stop executing is with the break statement.

First, create a `while` with a condition that is always true. The simplest way is shown.

Using an `if` statement, you define the stopping condition. Inside the `if`, you write `break`, meaning “exit the loop.”

The difference here is that this loop is guaranteed to run at least once.

### While / Else

Something completely different about Python is the `while/else` construction. `while/else` is similar to `if/else`, but there is a difference: the `else` block will execute **anytime** the loop condition is evaluated to `False`. This means that it will execute if the loop is never entered or if the loop exits normally. If the loop exits as the result of a `break`, the `else` will not be executed.

### For Loop

An alternative way to loop is the `for` loop. The syntax is as shown in the code editor. This example means “for each number `i` in the range 0 - 9, print `i`“.

``` python
print "Counting..."

for i in range(10):
  print i
```

This kind of loop is useful when you want to do something a certain number of times, such as append something to the end of a list.

Using a `for` loop, you can print out each individual character in a string.

### String Manipulation in For Loops

String manipulation is useful in for loops if you want to modify some content in a string.

``` python
word = "Marble"
for char in word:
  print char,
```

The example above iterates through each character in `word` and, in the end, prints out `M a r b l e`.

The `,` character after our `print` statement means that our next `print` statement keeps printing on the same line.

### Numbers Manipulation in For Loops

Perhaps the most useful (and most common) use of `for` loops is to go through a list.

On each iteration, the variable `num` will be the next value in the list. 

So, the first time through, it will be 7, the second time it will be `9`, then `12`, `54` and then the loop will exit when there are no more values in the list.

``` python
numbers = [7, 9, 12, 54]

for num in numbers:
  print num
```

### Looping Over a Dictionary

You may be wondering how looping over a dictionary would work. Would you get the key or the value?

The short answer is: you get the key which you can use to get the value.

```python
d = {'x': 9, 'y': 10, 'z': 20}

for key in d:
  if d[key] == 10:
    print "This dictionary has the value 10!"
``` 

First, we create a dictionary with strings as the keys and numbers as the values.
Then, we iterate through the dictionary, each time storing the key in `key`.
Next, we check if that key’s value is equal to 10.
If so, we print `"This dictionary has the value 10!"`

### Enumerate Index to Each Element in a List

At times it is useful to know how far into the list you are. Thankfully the built-in `enumerate` function helps with this.

`enumerate` works by supplying a corresponding index to each element in the list that you pass it. Each time you go through the loop, `index` will be one greater, and `item` will be the next item in the sequence. It’s very similar to using a normal `for` loop with a list, except this gives us an easy way to count how many items we’ve seen so far.

``` python
choices = ['pizza', 'pasta', 'salad', 'nachos']

print 'Your choices are:'
for index, item in enumerate(choices):
  print index + 1, item
```

### Multiple Lists

It’s also common to need to iterate over two lists at once. This is where the built-in `zip` function comes in handy.

`zip` will create pairs of elements when passed two lists, and will stop at the end of the shorter list.

`zip` can handle three or more lists as well!

``` python
list_a = [3, 9, 17, 15, 19]
list_b = [2, 4, 8, 10, 30, 40, 50, 60, 70, 80, 90]

for a, b in zip(list_a, list_b):
  # Add your code here!
  if a > b:
   print a
  else:
   print b
```

### For / Else

Just like with `while`, `for` loops may have an `else` associated with them.

In this case, the `else` statement is executed after the `for`, but only if the `for` ends normally—that is, not with a `break`. This code will break when it hits `'tomato'`, so the `else` block won’t be executed.

``` python
fruits = ['banana', 'apple', 'orange', 'tomato', 'pear', 'grape']

print 'You have...'
for f in fruits:
  if f == 'tomato':
    print 'A tomato is not a fruit!' # (It actually is.)
    break
  print 'A', f
else:
  print 'A fine selection of fruits!'
```

## 8. Advaced Topics in Python

### Iterators for Dictionaries

Let’s start with iterating over a dictionary. Recall that a dictionary is just a collection of keys and values.

``` python
d = {
  "Name": "Guido",
  "Age": 56,
  "BDFL": True
}
print d.items()
# => [('BDFL', True), ('Age', 56), ('Name', 'Guido')]
```

Note that the `.items()` method doesn’t return key/value pairs in any specific order.

### Keys() and Values()

While `.items()` returns an array of tuples with each tuple consisting of a key/value pair from the dictionary:

The `.keys()` method returns a list of the dictionary’s keys, and
The `.values()` method returns a list of the dictionary’s values.
Again, these methods will not return the keys or values from the dictionary in any specific order.

You can think of a tuple as an immutable (that is, unchangeable) list. Tuples are surrounded by `()`s and can contain any data type.

``` python
my_dict = {
  'name': 'Nick',
  'age':  31,
  'occupation': 'Dentist',
}

for key in my_dict:
  print key, my_dict[key]
``` 

### The 'in' Operator

For iterating over lists, tuples, dictionaries, and strings, Python also includes a special keyword: `in`. You can use in very `in`tuitively, like so:

``` python
for number in range(5):
  print number,

d = { 
  "name": "Eric",
  "age": 26
}

for key in d:
  print key, d[key],

for letter in "Eric":
  print letter,  # note the comma!
``` 

In the example above, first we create and iterate through a range, printing out `0 1 2 3 4`. Note that the trailing comma ensures that we keep printing on the same line.

Next, we create a dictionary and iterate through, printing out `age 26 name Eric`. Dictionaries have no specific order.

Finally, we iterate through the letters of a string, printing out `E r i c`.

### Building Lists (List Comprehension)

Let’s say you wanted to build a list of the numbers from 0 to 50 (inclusive). We could do this pretty easily:

``` python
my_list = range(51)
```

But what if we wanted to generate a list according to some logic—for example, a list of all the even numbers from 0 to 50?

Python’s answer to this is the **list comprehension**. List comprehensions are a powerful way to generate lists using the `for`/`in` and `if` keywords we’ve learned.

``` python
evens_to_50 = [i for i in range(51) if i % 2 == 0]
print evens_to_50
```

### List Comprehension Syntax 

Here’s a simple example of list comprehension syntax:

``` python
new_list = [x for x in range(1, 6)]
# => [1, 2, 3, 4, 5]
```

This will create a new_list populated by the numbers one to five. If you want those numbers doubled, you could use:

``` python
doubles = [x * 2 for x in range(1, 6)]
# => [2, 4, 6, 8, 10]
```

And if you only wanted the doubled numbers that are evenly divisible by three:

``` python
doubles_by_3 = [x * 2 for x in range(1, 6) if (x * 2) % 3 == 0]
# => [6]
```

### List Slicing Syntax

Sometimes we only want part of a Python list. Maybe we only want the first few elements; maybe we only want the last few. Maybe we want every other element!

List slicing allows us to access elements of a list in a concise manner. The syntax looks like this:

```python 
[start:end:stride]
```

Where `start` describes where the slice starts (inclusive), `end` is where it ends (exclusive), and `stride` describes the space between items in the sliced list. For example, a stride of `2` would select every other item from the original list to place in the sliced list.

### Omitting Indices

If you don’t pass a particular index to the list slice, Python will pick a default.

``` python
to_five = ['A', 'B', 'C', 'D', 'E']

print to_five[3:]
# prints ['D', 'E'] 

print to_five[:2]
# prints ['A', 'B']

print to_five[::2]
# print ['A', 'C', 'E']
```

The default starting index is `0`.
The default ending index is the end of the list.
The default stride is `1`.

### Reversing a List

We have seen that a positive stride progresses through the list from left to right.

A *negative* stride progresses through the list from right to left.

``` python
letters = ['A', 'B', 'C', 'D', 'E']
print letters[::-1]
```

In the example above, we print out `['E', 'D', 'C', 'B', 'A']`.

## 9. Introduction to Classes

### Why Use Classes?

Python is an object-oriented programming language, which means it manipulates programming constructs called *objects*. You can think of an object as a single data structure that contains data as well as functions; the functions of an object are called its methods. For example, any time you call

```python
len("Eric")
```

Python is checking to see whether the string object you passed it has a length, and if it does, it returns the value associated with that `attribute`. When you call

```python
my_dict.items()
```

Python checks to see if `my_dict` has an `items()` method (which all dictionaries have) and executes that method if it finds it.

But what makes `"Eric"` a string and `my_dict` a dictionary? The fact that they’re instances of the `str` and `dict` classes, respectively. A class is just a way of organizing and producing objects with similar attributes and methods.

### Class Syntax

A basic class consists only of the `class` keyword, the name of the class, and the class from which the new class *inherits* in parentheses. (We’ll get to inheritance soon.) 

For now, our classes will inherit from the `object` class, like so:

``` python
class NewClass(object):
  # Class magic here
```

This gives them the powers and abilities of a Python object. By convention, user-defined Python class names start with a capital letter.

### Classier Classes

We’d like our classes to do *nothing*, so we’ll have to replace our `pass` with something else.

You may have noticed in our example back in the first exercise that we started our class definition off with an odd-looking function: `__init__()`. 

This function is required for classes, and it’s used to initialize the objects it creates. `__init__()` always takes at least one argument, `self`, that refers to the object being created. 

You can think of `__init__()` as the function that “boots up” each object the class creates.

Let’s make one more tweak to our class definition, then go ahead and **instantiate** (create) our first object.

So far, `__init__()` only takes one parameter: `self`. This is a Python convention; there’s nothing magic about the word `self`. However, it’s overwhelmingly common to use `self` as the first parameter in `__init__()`, so you should do this so that other people will understand your code.

The part that is magic is the fact that `self` is the first parameter passed to `__init__()`. Python will use the first parameter that `__init__()` receives to refer to the object being created; this is why it’s often called `self`, since this parameter gives the object being created its identity.

### Instantiating Your First Object

Now we’re ready to start creating objects. 

We can access attributes of our objects using dot notation. Here’s how it works:

```python
class Square(object):
  def __init__(self):
    self.sides = 4

my_shape = Square()
print my_shape.sides
```

First we create a class named `Square` with an attribute `sides`.

Outside the class definition, we create a new instance of `Square` named `my_shape` and access that attribute using `my_shape.sides`.

### More on __init__() and self

Now that you’re starting to understand how classes and objects work, it’s worth delving a bit more into `__init__()` and `self`. They can be confusing!

As mentioned, you can think of `__init__()` as the method that “boots up” a class’ instance object: the `init` bit is short for “initialize.”

The first argument `__init__()` gets is used to refer to the instance object, and by convention, that argument is called `self`. 

If you add additional arguments—for instance, a `name` and `age` for your animal—setting each of those equal to `self.name` and `self.age` in the body of `__init__()` will make it so that when you create an instance object of your `Animal` class, you need to give each instance a name and an age, and those will be associated with the particular instance you create.

### Class Scope

Another important aspect of Python classes is *scope*. The scope of a variable is the context in which it’s visible to the program.

It may surprise you to learn that not all variables are accessible to all parts of a Python program at all times. When dealing with classes, you can have variables that are available everywhere (*global variables*), variables that are only available to members of a certain class (*member variables*), and variables that are only available to particular instances of a class (*instance variables*).

The same goes for functions: some are available everywhere, some are only available to members of a certain class, and still others are only available to particular instance objects.

### A Methodical Approach

When a class has its own functions, those functions are called *methods*. You’ve already seen one such method: `__init__()`. But you can also define your own methods!

``` python
class Animal(object):
  """Makes cute animals."""
  is_alive = True
  def __init__(self, name, age):
    self.name = name
    self.age = age
  def description(self):
    print self.name
    print self.age

hippo = Animal ("Boiro", 5)

print hippo.description()
```

### Member Variables of a Class

A class can have any number of **member variables**. These are variables that are available to all members of a class.

``` python
hippo = Animal("Jake", 12)
cat = Animal("Boots", 3)
print hippo.is_alive
hippo.is_alive = False
print hippo.is_alive
print cat.is_alive
```

In the example above, we create two instances of an `Animal`.

Then we print out `True`, the default value stored in hippo’s `is_alive` member variable.

Next, we set that to False and print it out to make sure.

Finally, we print out `True`, the value stored in cat’s `is_alive` member variable. We only changed the variable in hippo, not in cat.

Let’s add another member variable to `Animal`.

### Inheritance

*Inheritance* is a tricky concept, so let’s go through it step by step.

Inheritance is the process by which one class takes on the attributes and methods of another, and it’s used to express an *is-a* relationship. 

For example, a Panda is a bear, so a Panda class could inherit from a Bear class. However, a Toyota is not a Tractor, so it shouldn’t inherit from the Tractor class (even if they have a lot of attributes and methods in common). Instead, both Toyota and Tractor could ultimately inherit from the same Vehicle class.

``` python
class Customer(object):
  """Produces objects that represent customers."""
  def __init__(self, customer_id):
    self.customer_id = customer_id

  def display_cart(self):
    print "I'm a string that stands in for the contents of your shopping cart!"

class ReturningCustomer(Customer):
  """For customers of the repeat variety."""
  def display_order_history(self):
    print "I'm a string that stands in for your order history!"

monty_python = ReturningCustomer("ID: 12345")
monty_python.display_cart()
monty_python.display_order_history()
```

### Inheritance Syntax

In Python, inheritance works like this:

``` python
class DerivedClass(BaseClass):
  # code goes here
```

where *DerivedClass* is the new class you’re making and *BaseClass* is the class from which that new class inherits.

``` python
class Shape(object):
  """Makes shapes!"""
  def __init__(self, number_of_sides):
    self.number_of_sides = number_of_sides

# Add your Triangle class below!
class Triangle(Shape):
  def __init__(self, side1, side2, side3):
    self.side1 = side1
    self.side2 = side2
    self.side3 = side3
```

### Override Classes

Sometimes you’ll want one class that inherits from another to not only take on the methods and attributes of its parent, but to *override* one or more of them.

``` python
class Employee(object):
  def __init__(self, name):
    self.name = name
  def greet(self, other):
    print "Hello, %s" % other.name

class CEO(Employee):
  def greet(self, other):
    print "Get back to work, %s!" % other.name

ceo = CEO("Emily")
emp = Employee("Steve")
emp.greet(ceo)
# Hello, Emily
ceo.greet(emp)
# Get back to work, Steve!
```

Rather than have a separate `greet_underling` method for our CEO, we override (or re-create) the `greet` method on top of the base `Employee.greet` method. This way, we don’t need to know what type of Employee we have before we greet another Employee.

### Superclass

Sometimes you’ll be working with a **derived class (or subclass**) and realize that you’ve overwritten a method or attribute defined in that class’ base class (also called a parent or superclass) that you actually need. 

You can directly access the attributes or methods of a superclass with Python’s built-in `super` call.

The syntax looks like this:

```python
class Derived(Base):
  def m(self):
    return super(Derived, self).m()
```

Where `m()` is a method from the base class.



[Python Standard Library](https://docs.python.org/3/library/index.html#library-index)

## Compound Statement

- [The if Statement](https://docs.python.org/3/reference/compound_stmts.html#the-if-statement)
- [The while Statement](https://docs.python.org/3/reference/compound_stmts.html#the-while-statement)
- [The for Statement](https://docs.python.org/3/reference/compound_stmts.html#the-for-statement)
- [The try Statement](https://docs.python.org/3/reference/compound_stmts.html#the-try-statement)

