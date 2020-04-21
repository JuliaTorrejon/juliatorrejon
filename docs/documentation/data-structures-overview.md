# Data Structures Overview

!!! Data-Structures
    A data structure is a particular way of organizing data in a computer so that it can be used effectively.

![Image by N@vinkumar Dhopre](http://2.bp.blogspot.com/-HaT14cTrndU/Vf6FUS7z7qI/AAAAAAAAAYI/lkm_eFkowFo/s1600/data%2Bstructure.jpg)

## Overview of Data Structures

Working with programming algorithms often goes hand-in-hand with an associated set of data structures. After all, most algorithms are intented to work with data and that data has to be represented somewhere.

Data structures are:

- Used to organise data so it can be processed

The data structures that you will probably most commonly work with are arrays, linked lists, stacks and queues, trees and hash tables.

Here's a list of the absolute, must-have knowledge:

| Data Structures       | Algorithms           | 
| -------------         |:-------------:       | 
| Linked Lists          | Breadth First Search | 
| Binary Trees          | Depth First Search   | 
| Tries                 | Binary Search        | 
| Stacks                | Merge Sort           | 
| Queues                | Quick Sort           |
| Vectors / Array Lists | Tree Insert, etc     | 
| Hash Tables           |                      | 

![Image by Eric Rowell](https://s2.ax1x.com/2019/11/22/M7VTHK.png)

## Arrays

Collection of elements identified by index or key value. In a simpler form, an array just contains a linear set of values, which is often called a **one-dimensional** array.

One of the features of an array is that element positions can be calculated using a mathematical expression and this enables array elements to be accessed directly in what is usually called **random access fashion**. 

In other words, since the position of each element can be direclty computed, it's not necessary to navigate the data structure in order to access a particular element. 

### Array Operations

- Calculate item index: O(1) is a constant time operation since it's not dependent on how many items are in the array
- Insert or delete item at beginning: O(n) takes time complexity
- Insert or delete item in the middle: O(n) takes time complexity since the middle items must be moved to their new memory locations
- Insert or delete item at end O(1) can be done in constant time


### Resources

[Practical Algorithms & Data Structures](https://bradfieldcs.com/algos/recursion/dynamic-programming/)
[Data Structures - Python Docs](https://docs.python.org/3/tutorial/datastructures.html)
[Big O Cheat Sheet](https://www.bigocheatsheet.com/)