# Object Oriented Programming

Object-oriented programming (OOP) is a programming language that is used to solve problems by thinking in terms of real-world objects or data rather than functions and logic.

Additional benefits of OOP include code **reusability**, **scalability** and **efficiency**.

## Principles of OOP

Object-oriented programming is based on the following concepts and fundamentals:

### Inheritance

Inheritance is a way of creating new class for using details of existing class without modifying it. 

The newly formed class is a derived class (or child class). Similarly, the existing class is a base class (or parent class).

### Encapsulation

Hiding the private details of a class from other objects. We can restrict access to methods and variables. This prevents data from direct modification. In Python, we denote private attribute using underscore as prefix i.e single “ _ “ or double “ __“.

### Polymorphism

Polymorphism is an ability to use common interface for multiple form (data types).

### Class

A class is a holding structure which is used to create an object, also called a blueprint for an object. 

It holds attributes that make the state of object and methods which can be called upon those objects.  A class can hold both static and non-static methods.

The simplest form of class definition looks like this:

``` python
class ClassName:
    <statement-1>
    .
    .
    .
    <statement-N>
```

#### Class Definition Syntax

Class definitions, like function definitions (def statements) must be executed before they have any effect. 

In practice, the statements inside a class definition will usually be function definitions. The function definitions inside a class normally have a peculiar form of argument list, dictated by the calling conventions for methods.

When a class definition is entered, a new namespace is created, and used as the local scope — thus, all assignments to local variables go into this new namespace. In particular, function definitions bind the name of the new function here.

When a class definition is left normally (via the end), a class object is created. The original local scope (the one in effect just before the class definition was entered) is reinstated, and the class object is bound here to the class name given in the class definition header (`ClassName` in the example).

### Class Objects

An object is what you create from Class. You can create multiple instances of objects from a single class. Each object has values for the attributes which define their state. 

When class is defined, only the description for the object is defined. Therefore, no memory or storage is allocated.

*Class objects* support two kinds of operations: attribute references and instantiation.

Attribute references use the standard syntax used for all attribute references in Python: obj.name. Valid attribute names are all the names that were in the class’s namespace when the class object was created. So, if the class definition looked like this:

``` python
class MyClass:
    """A simple example class"""
    i = 12345

    def f(self):
        return 'hello world'
```
Then `MyClass.i` and `MyClass.f` are valid attribute references, returning an integer and a function object, respectively. Class attributes can also be assigned to, so you can change the value of `MyClass.i` by assignment. __doc__ is also a valid attribute, returning the docstring belonging to the class: `"A simple example class"`.

*Class instantiation* uses function notation. Just pretend that the class object is a parameterless function that returns a new instance of the class. For example (assuming the above class):

```python 
x = MyClass()
```

Creates a new instance of the class and assigns this object to the local variable `x`.

The instantiation operation (“calling” a class object) creates an empty object. Many classes like to create objects with instances customized to a specific initial state. Therefore a class may define a special method named __init__(), like this:

``` python
def __init__(self):
    self.data = []
```
When a class defines an __init__() method, class instantiation automatically invokes __init__() for the newly-created class instance. So in this example, a new, initialized instance can be obtained by:

``` python
x = MyClass()
```

Of course, the __init__() method may have arguments for greater flexibility. In that case, arguments given to the class instantiation operator are passed on to __init__(). For example,

``` python
>>> class Complex:
...     def __init__(self, realpart, imagpart):
...         self.r = realpart
...         self.i = imagpart
...
>>> x = Complex(3.0, -4.5)
>>> x.r, x.i
(3.0, -4.5)
```

### Instance Objects
Now what can we do with instance objects? The only operations understood by instance objects are attribute references. There are two kinds of valid attribute names, *data attributes* and *methods*.

Data attributes need not be declared; like local variables, they spring into existence when they are first assigned to. For example, if x is the instance of MyClass created above, the following piece of code will print the value 16, without leaving a trace:

``` python
x.counter = 1
while x.counter < 10:
    x.counter = x.counter * 2
print(x.counter)
del x.counter
```

The other kind of instance attribute reference is a method. A method is a function that “belongs to” an object. (In Python, the term method is not unique to class instances: other object types can have methods as well. For example, list objects have methods called append, insert, remove, sort, and so on. However, in the following discussion, we’ll use the term method exclusively to mean methods of class instance objects, unless explicitly stated otherwise.)

Valid method names of an instance object depend on its class. By definition, all attributes of a class that are function objects define corresponding methods of its instances. So in our example, x.f is a valid method reference, since MyClass.f is a function, but x.i is not, since MyClass.i is not. But x.f is not the same thing as MyClass.f — it is a method object, not a function object.

### Method Objects

Methods are functions defined inside the body of a class. They are used to define the behaviors of an object.

Usually, a method is called right after it is bound:

``` python
x.f()
```

In the MyClass example, this will return the string 'hello world'. However, it is not necessary to call a method right away: x.f is a method object, and can be stored away and called at a later time. For example:

``` python
xf = x.f
while True:
    print(xf())
```

will continue to print hello world until the end of time.

What exactly happens when a method is called? You may have noticed that x.f() was called without an argument above, even though the function definition for f() specified an argument. What happened to the argument? Surely Python raises an exception when a function that requires an argument is called without any — even if the argument isn’t actually used…

Actually, you may have guessed the answer: the special thing about methods is that the instance object is passed as the first argument of the function. In our example, the call x.f() is exactly equivalent to MyClass.f(x). In general, calling a method with a list of n arguments is equivalent to calling the corresponding function with an argument list that is created by inserting the method’s instance object before the first argument.

If you still don’t understand how methods work, a look at the implementation can perhaps clarify matters. When a non-data attribute of an instance is referenced, the instance’s class is searched. If the name denotes a valid class attribute that is a function object, a method object is created by packing (pointers to) the instance object and the function object just found together in an abstract object: this is the method object. When the method object is called with an argument list, a new argument list is constructed from the instance object and the argument list, and the function object is called with this new argument list.

### Class and Instance Variables

Generally speaking, instance variables are for data unique to each instance and class variables are for attributes and methods shared by all instances of the class:

``` python
class Dog:

    kind = 'canine'         # class variable shared by all instances

    def __init__(self, name):
        self.name = name    # instance variable unique to each instance

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.kind                  # shared by all dogs
'canine'
>>> e.kind                  # shared by all dogs
'canine'
>>> d.name                  # unique to d
'Fido'
>>> e.name                  # unique to e
'Buddy'
```

As discussed in A Word About Names and Objects, shared data can have possibly surprising effects with involving mutable objects such as lists and dictionaries. For example, the tricks list in the following code should not be used as a class variable because just a single list would be shared by all Dog instances:

``` python
class Dog:

    tricks = []             # mistaken use of a class variable

    def __init__(self, name):
        self.name = name

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks                # unexpectedly shared by all dogs
['roll over', 'play dead']
```

Correct design of the class should use an instance variable instead:

``` python
class Dog:

    def __init__(self, name):
        self.name = name
        self.tricks = []    # creates a new empty list for each dog

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks
['roll over']
>>> e.tricks
['play dead']
```












References: [The Python Tutorial](https://docs.python.org/3/tutorial/classes.html#a-first-look-at-classes)