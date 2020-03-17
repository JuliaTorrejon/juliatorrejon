# Data Strcutures

A data structure is a particular way of organizing data in a computer so that it can be used effectively. 

![Image by N@vinkumar Dhopre](http://2.bp.blogspot.com/-HaT14cTrndU/Vf6FUS7z7qI/AAAAAAAAAYI/lkm_eFkowFo/s1600/data%2Bstructure.jpg)

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

# Lists

A list is a collection of items where each item holds a relative position with respect to the others.

The members of a list are commonly refered to as **nodes**. When each node holds a reference to the next node in the list, we call this a singly linked list. When each node holds a reference to both the next and previous nodes in the list, we call this a doubly linked list.

We will consider that there are two types of lists: **unordered and ordered lists**. As we will see, an ordered list is simply a list with additional functionality designed to maintain its constituent nodes in a particular order.

## Unordered List
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





### Resources

- [Practical Algorithms & Data Structures](https://bradfieldcs.com/algos/recursion/dynamic-programming/)
- [Data Structures - Python Docs](https://docs.python.org/3/tutorial/datastructures.html)
- [Big O Cheat Sheet](https://www.bigocheatsheet.com/)