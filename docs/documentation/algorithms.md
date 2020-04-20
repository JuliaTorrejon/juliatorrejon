# Algorithms

!!! Algorithms
    Algorithm analysis is a way to compare the time and space efficiency of programs with respect to their possible inputs, but irrespective of other context.
    
![Image by Eric Rowell](https://miro.medium.com/max/596/1*ipkeWQ_Lb0lbkhB8rigxTA.png)

## Algorithm Characteristics

**Algorithm Complexity**

- *Space Compexity*: How much memory does it require?
- *Time Complexity*: How much time does it take to complete?

**Inputs and Outputs**

- What does the algorithm accept, and what are the results?

## Common Algorithms

We can investigate some of the more common algorithms that appear in a variety of programming scenarios:

### Search Algorithms

- Find specific data in a structure (for example, a substring within a string)

### Sorting Algorithms

- Take a dataset and apply a sort order to it

### Computation Algorithms

- Given one set of data, calculate another (is a given number prime?)

### Collection Algorithms

- Work with collections of data (count specific items, navigate among data elements, filter out unwanted data, etc)

## Understanding Algorithm Performance

This is an important factor in how you choose a particular algorithm to solve a programming problem as well as understanding how your programme will behave under different circumstances.

- Measure how an algorithm responds to dataset size
- Big O Notation (used to describe algorithm performance)
    - Classifies performance as the input size grows
    - "O" indicates *the order of operation*: time scale to perform an operation (it usually describes the worst case scenario of how long it takes to perform a given operation)
- Many algorithms and data structures have more than one O
    - Data structure can use multiple types of operations such as inserting data, searching for data, deleting data, etc. 

## Big O Notations

![Image by Eric Rowell](https://miro.medium.com/max/1464/1*5ZLci3SuR0zM_QlZOADv8Q.jpeg)

## Commom Big-O Terms

Listed Big-O Notations in an ascending order of time complexity.

| Notation   | Description   | Example                                                                            |
|------------|---------------|------------------------------------------------------------------------------------|
| O(1)       | Constant time | Looking up a single element in an array                                            |
| O(log n)   | Logarithmic   | Finding an item in a sorted array with a binary search                             |
| O(n)       | Linear time   | Searching an unsorted array for a specific value                                   |
| O(n log n) | Long-linear   | Complex sorting algorithms like heap sort and merge sort                           |
| O(n^2)     | Quadratic     | Simple sorting algorithms, such as bubble sort, selection sort, and insertion sort | 

- **O(1)**: This notation means that the operation in question doesn't depend on the number of elements in the given data set. A good example is calculating if a number is even or odd, or looking up for a specific element index in an array.
- **O(log n)**: A typical example of this kind of operation is finding a specific value in a sorted array using binary search, so as the number of items in the sorted array grows, it only takes a logarithim time relationship to find any given item. 
- **O(n)**: This level of time complexity corresponds to a typical example of searching for an item in an unsorted array, so as more items are added to the array in an unsorted fashion, it corresponds a linear amount of time to perform a search. 
- **O(n log n)**: It's called *n times log n* or long-linear time complexity. Some good examples of this kind of operation are some sorting algorithms like heap sort and merge sort.
- **O(n^2)**: It's not a very good level of performance because what that means is as the number of items in the data set increases, the time it takes to process them increases at the square of that number. Some examples of this type of operation are some of the simpler sorting algorithms like the bubble sort and the selection sort.

## Performance of Python Types

This is the big O notation performance for the most commonly-used operations supported by Python lists and dictionaries.

### Lists

The designers of the Python list data type had many choices to make during implementation. Each choice affected how quickly the list could perform operations. One decision they made was to optimize the list implementation for common operations.

### Indexing & Assigning

Two common operations are indexing and assigning to an index position. In Python lists, values are assigned to and retrieved from specific, known memory locations. No matter how large the list is, index lookup and assignment take a constant amount of time and are thus O(1)O(1).

### Appending & Concatenating

Another common programming need is to grow a list. There are two ways to do this: you can use the append method or the concatenation operator (+).

The append method is “amortized” O(1)O(1). In most cases, the memory required to append a new value has already been allocated, which is strictly O(1)O(1). Once the C array underlying the list has been exhausted, it must be expanded in order to accomodate further appends. This periodic expansion process is linear relative to the size of the new array, which seems to contradict our claim that appending is O(1)O(1).

However, the expansion rate is cleverly chosen to be three times the previous size of the array; when we spread the expansion cost over each additional append afforded by this extra space, the cost per append is O(1)O(1) on an amortized basis.

On the other hand, concatenation is O(k)O(k), where kk is the size of the concatenated list, since kk sequential assignment operations must occur.

### Popping, Shifting & Deleting

Popping from a Python list is typically performed from the end but, by passing an index, you can pop from a specific position. When pop is called from the end, the operation is O(1)O(1), while calling pop from anywhere else is O(n)O(n). Why the difference?

When an item is taken from the front of a Python list, all other elements in the list are shifted one position closer to the beginning. This is an unavoidable cost to allow O(1)O(1) index lookup, which is the more common operation.

For the same reasons, inserting at an index is O(n)O(n); every subsequent element must be shifted one position closer to the end to accomodate the new element. Unsurprisingly, deletion behaves the same way.

### Iteration

Iteration is O(n)O(n) because iterating over nn elements requires nn steps. This also explains why the in operator in Python is O(n)O(n): to determine whether an element is in a list, we must iterate over every element.

### Slicing

Slice operations require more thought. To access the slice [a:b] of a list, we must iterate over every element between indices a and b. So, slice access is O(k)O(k), where kk is the size of the slice. Deleting a slice is O(n)O(n) for the same reason that deleting a single element is O(n)O(n): nn subsequent elements must be shifted toward the list's beginning.

### Multiplying

To understand list multiplication, remember that concatenation is O(k)O(k), where kk is the length of the concatenated list. It follows that multiplying a list is O(nk)O(nk), since multiplying a kk-sized list nn times will require k(n - 1)k(n−1) appends.

### Reversing

Reversing a list is O(n)O(n) since we must reposition each element.

### Sorting

Finally (and least intuitively), sorting in Python is O(n\log{n})O(nlogn) and beyond the scope of this book to demonstrate.

For reference, we’ve summarized the performance characteristics of Python's list operations in the table below:

| **Operation**       | **Big O Efficiency** | 
| -------------       |:-------------:       | 
| index []            | O(1)                 | 
| index assignment    | O(1)                 | 
| append              | O(1)                 |
| pop()               | O(1)                 | 
| pop(i)              | O(n)                 | 
| insert(i, ittem)    | O(n)                 |
| del operator        | O(n)                 | 
| iteration           | O(n)                 | 
| contains (in)       | O(n)                 |
| get slice [x:y]     | O(k)                 | 
| del slice           | O(n)                 | 
| reverse             | O(n)                 |
| concatenate         | O(k)                 | 
| sort                | O(n log n)           | 
| multiply            | O(nk)                |


### Resources

[Big O Cheat Sheet](https://www.bigocheatsheet.com/)