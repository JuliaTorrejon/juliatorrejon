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

### Method

Methods are functions defined inside the body of a class. They are used to define the behaviors of an object.



References:[The Python Tutorial](https://docs.python.org/3/tutorial/classes.html#a-first-look-at-classes)