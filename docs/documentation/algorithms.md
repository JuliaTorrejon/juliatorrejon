# Algorithms

![Image by Eric Rowell](https://miro.medium.com/max/596/1*ipkeWQ_Lb0lbkhB8rigxTA.png)

## Big O Notations

![Image by Eric Rowell](https://miro.medium.com/max/1464/1*5ZLci3SuR0zM_QlZOADv8Q.jpeg)


### Performance of Python Types

This is the big O notation performance for the most commonly-used operations supported by Python lists and dictionaries.

#### Lists
The designers of the Python list data type had many choices to make during implementation. Each choice affected how quickly the list could perform operations. One decision they made was to optimize the list implementation for common operations.

#### Indexing & Assigning
Two common operations are indexing and assigning to an index position. In Python lists, values are assigned to and retrieved from specific, known memory locations. No matter how large the list is, index lookup and assignment take a constant amount of time and are thus O(1)O(1).

#### Appending & Concatenating
Another common programming need is to grow a list. There are two ways to do this: you can use the append method or the concatenation operator (+).

The append method is “amortized” O(1)O(1). In most cases, the memory required to append a new value has already been allocated, which is strictly O(1)O(1). Once the C array underlying the list has been exhausted, it must be expanded in order to accomodate further appends. This periodic expansion process is linear relative to the size of the new array, which seems to contradict our claim that appending is O(1)O(1).

However, the expansion rate is cleverly chosen to be three times the previous size of the array; when we spread the expansion cost over each additional append afforded by this extra space, the cost per append is O(1)O(1) on an amortized basis.

On the other hand, concatenation is O(k)O(k), where kk is the size of the concatenated list, since kk sequential assignment operations must occur.

#### Popping, Shifting & Deleting
Popping from a Python list is typically performed from the end but, by passing an index, you can pop from a specific position. When pop is called from the end, the operation is O(1)O(1), while calling pop from anywhere else is O(n)O(n). Why the difference?

When an item is taken from the front of a Python list, all other elements in the list are shifted one position closer to the beginning. This is an unavoidable cost to allow O(1)O(1) index lookup, which is the more common operation.

For the same reasons, inserting at an index is O(n)O(n); every subsequent element must be shifted one position closer to the end to accomodate the new element. Unsurprisingly, deletion behaves the same way.

#### Iteration
Iteration is O(n)O(n) because iterating over nn elements requires nn steps. This also explains why the in operator in Python is O(n)O(n): to determine whether an element is in a list, we must iterate over every element.

#### Slicing
Slice operations require more thought. To access the slice [a:b] of a list, we must iterate over every element between indices a and b. So, slice access is O(k)O(k), where kk is the size of the slice. Deleting a slice is O(n)O(n) for the same reason that deleting a single element is O(n)O(n): nn subsequent elements must be shifted toward the list's beginning.

#### Multiplying
To understand list multiplication, remember that concatenation is O(k)O(k), where kk is the length of the concatenated list. It follows that multiplying a list is O(nk)O(nk), since multiplying a kk-sized list nn times will require k(n - 1)k(n−1) appends.

#### Reversing
Reversing a list is O(n)O(n) since we must reposition each element.

#### Sorting
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