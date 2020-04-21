# Linked Lists

- Collection of data elements, called nodes (sort of similar like an array)
- Each of these nodes contains reference to the next element(node) in the list
- Each of these elements can contain whatever information your app needs to work with

The first element is called **the head** and each element has a field that refers to the next item in the list.
The last elemnetn in the list has a field point to nothing which indicates that it's the end of the list.

The diagram can be represented as a **sinlgy-linked list** which means that there's only one direction of links provided, that is, each item only knows about its next neighbour. 

O as a **double-linked list**, in this case each data item has a reference to both, the previous and the next items that are neighbours.

## Linked Lists vs Arrays

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