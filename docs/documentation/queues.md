# Queues

- **Queues**: Collection that supports adding and removing items but it operates in a **first-in, first-out** method
- Order processing is a good used for a queue becauses it ensures that orders for a product are fulfilled in the order in that they were received by the system
- Message processing, when using your phone's SMS messenger app entering each message, you want to make sure that each of those messages is sent in the order they were written. The messenger app might use a queue to maintain each message and make sure that they are sent in the order they were placed into the queue.

The queue operations are:

- **Queue()** creates a new queue that is empty. It needs no parameters and returns an empty queue.
- **enqueue(item)** adds a new item to the rear of the queue. It needs the item and returns nothing.
- **dequeue()** removes the front item from the queue. It needs no parameters and returns the item. The queue is modified.
- **is_empty()** tests to see whether the queue is empty. It needs no parameters and returns a boolean value.
- **size()** returns the number of items in the queue. It needs no parameters and returns an integer.