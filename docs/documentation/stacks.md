# Stacks

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