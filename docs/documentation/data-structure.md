# Data Structures

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

## Linked Lists

- Collection of data elements, called nodes (sort of similar like an array)
- Each of these nodes contains reference to the next element(node) in the list
- Each of these elements can contain whatever information your app needs to work with

The first element is called **the head** and each element has a field that refers to the next item in the list.
The last elemnetn in the list has a field point to nothing which indicates that it's the end of the list.

The diagram can be represented as a **sinlgy-linked list** which means that there's only one direction of links provided, that is, each item only knows about its next neighbour. 

O as a **double-linked list**, in this case each data item has a reference to both, the previous and the next items that are neighbours.

### Linked Lists vs Arrays

| Basis for  Comparison              | Array                                                                     | Linked List                                                                                    |   |   |
|------------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|---|---|
| Basic                              | It is a consistent set of a fixed number of data items                    | It is an unordered set comprising a variable number of data items                              |   |   |
| Size                               | Specified during declaration                                              | No need to specify; grow and shrink during execution                                           |   |   |
| Storage Allocation                 | Element location is allocated during compile time                         | Element position is assigned during run time                                                   |   |   |
| Order of the Elements              | Stored consecutively                                                      | Stored randomly                                                                                |   |   |
| Accessing the  Elements            | Directly or randomly accessed, i.e., Specify the array index or subscript | Sequentially accessed, i.e., Traverse starting from the first  node in the list by the pointer |   |   |
| Insertion and  Deletion of Element | Slow relatively as shifting is required                                   | Easier, fast and efficient                                                                     |   |   |
| Searching                          | Binar search and linear search                                            | Linear search                                                                                  |   |   |
| Memory Required                    | Less                                                                      | More                                                                                           |   |   |
| Memory  Utilisation                | Ineffective                                                               | Efficient                                                                                      |   |   |

## Lists

A list is a collection of items where each item holds a relative position with respect to the others.

The members of a list are commonly refered to as **nodes**. When each node holds a reference to the next node in the list, we call this a singly linked list. When each node holds a reference to both the next and previous nodes in the list, we call this a doubly linked list.

We will consider that there are two types of lists: **unordered and ordered lists**. As we will see, an ordered list is simply a list with additional functionality designed to maintain its constituent nodes in a particular order.

### Unordered List

The structure of an unordered list, as described above, is a collection of items where each item holds a relative position with respect to the others. Some possible unordered list operations are given below.

- **list()** creates a new list that is empty. It needs no parameters and returns an empty list.
- **add(item)** adds a new item to the list. It needs the item and returns nothing. Assume the item is not already in the list.
- **remove(item)** removes the item from the list. It needs the item and modifies the list. Assume the item is present in the list.
- **search(item)** searches for the item in the list. It needs the item and returns a boolean value.
- **is_empty()** tests to see whether the list is empty. It needs no parameters and returns a boolean value.
- **size()** returns the number of items in the list. It needs no parameters and returns an integer.
- **append(item)** adds a new item to the end of the list making it the last item in the collection. It needs the item and returns nothing. Assume the item is not already in the list.
- **index(item)** returns the position of item in the list. It needs the item and returns the index. Assume the item is in the list.
- **insert(pos, item)** adds a new item to the list at position pos. It needs the item and returns nothing. Assume the item is not already in the list and there are enough existing items to have position pos.
- **pop()** removes and returns the last item in the list. It needs nothing and returns an item. Assume the list has at least one item.
- **pop(pos)** removes and returns the item at position pos. It needs the position and returns the item. Assume the item is in the list.

## Stacks and Queues

- **Stack**: Collection that supports two principle operations: push and pop and it operates in **last-in, first-out** data structures which means the last item pushed in the first one popped
- Are often used to parse and evaluate various forms of expression statements
- Backtracking: Browser back stack, for example. A good example of this is when you're using the back button in your browser, so as you click on the various links in the page, the browser adds each link to a stack in order to maintain the order in which they were visited so when a user clicks on the back button, the most recenlty added URL is popped off the stack and then revisited


The interface for a stack is:

- **Stack()** creates a new, empty stack
- **push(item)** adds the given item to the top of the stack and returns nothing
- **pop()** removes and returns the top item from the stack
- **peek()** returns the top item from the stack but doesn’t remove it (the stack isn’t modified)
- **is_empty()** returns a boolean representing whether the stack is empty
- **size()** returns the number of items on the stack as an integer


- **Queues**: Collection that supports adding and removing items but it operates in a **first-in, first-out** method
- Order processing is a good used for a queue becauses it ensures that orders for a product are fulfilled in the order in that they were received by the system
- Message processing, when using your phone's SMS messenger app entering each message, you want to make sure that each of those messages is sent in the order they were written. The messenger app might use a queue to maintain each message and make sure that they are sent in the order they were placed into the queue.

The queue operations are:

- **Queue()** creates a new queue that is empty. It needs no parameters and returns an empty queue.
- **enqueue(item)** adds a new item to the rear of the queue. It needs the item and returns nothing.
- **dequeue()** removes the front item from the queue. It needs no parameters and returns the item. The queue is modified.
- **is_empty()** tests to see whether the queue is empty. It needs no parameters and returns a boolean value.
- **size()** returns the number of items in the queue. It needs no parameters and returns an integer.


- **Deques**: A deque is structured, as an ordered collection of items where items are added and removed from either end, either front or rear

The deque operations are given below.

- **Deque()** creates a new deque that is empty. It needs no parameters and returns an empty deque.
- **add_front(item)** adds a new item to the front of the deque. It needs the item and returns nothing.
- **add_rear(item)** adds a new item to the rear of the deque. It needs the item and returns nothing.
- **remove_front()** removes the front item from the deque. It needs no parameters and returns the item. The deque is modified.
- **remove_rear()** removes the rear item from the deque. It needs no parameters and returns the item. The deque is modified.
- **is_empty()** tests to see whether the deque is empty. It needs no parameters and returns a boolean value.
- **size()** returns the number of items in the deque. It needs no parameters and returns an integer.



























### Resources

- [Practical Algorithms & Data Structures](https://bradfieldcs.com/algos/recursion/dynamic-programming/)
- [Data Structures - Python Docs](https://docs.python.org/3/tutorial/datastructures.html)
- [Big O Cheat Sheet](https://www.bigocheatsheet.com/)