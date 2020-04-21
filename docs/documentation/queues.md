# Queues

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