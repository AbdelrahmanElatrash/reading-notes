#  Stacks and Queues

## Stacks

A stack is a data structure that stores a collection of elements in a particular order. The order is commonly referred to as Last-In-First-Out (LIFO), which means that the last element added to the stack is the first one to be removed.

Stacks have two primary operations: push and pop. The push operation adds an element to the top of the stack, while the pop operation removes the top element from the stack.

Here's an example of a stack in Python using a list:

`stack = []`

`# Push some elements onto the stack`
`stack.append(1)`
`stack.append(2)`
`stack.append(3)`

`# Pop an element off the stack`
`top = stack.pop()`
`print(top)  # Output: 3`

`# The stack now contains [1, 2]`

In this example, we create an empty list to represent the stack. We then use the append method to add three elements to the stack (1, 2, and 3), and then use the pop method to remove the top element (3). The resulting stack contains the elements 1 and 2.

Stacks are commonly used in computer science and programming, especially in algorithms and data processing tasks. They can also be used in real-world scenarios, such as managing the history of web pages in a web browser or managing a pile of plates in a restaurant.

## Queues

A queue is a linear data structure that stores a collection of elements in a particular order. The order is commonly referred to as First-In-First-Out (FIFO), which means that the first element added to the queue is the first one to be removed.

Queues have two primary operations: enqueue and dequeue. The enqueue operation adds an element to the back of the queue, while the dequeue operation removes the element at the front of the queue.

Here's an example of a queue in Python using a list:

`queue = []`

`# Enqueue some elements`
`queue.append(1)`
`queue.append(2)`
`queue.append(3)`

`# Dequeue an element`
`front = queue.pop(0)`
`print(front)  # Output: 1`

`# The queue now contains [2, 3]`

In this example, we create an empty list to represent the queue. We then use the append method to add three elements to the queue (1, 2, and 3), and then use the pop(0) method to remove the element at the front of the queue (1). The resulting queue contains the elements 2 and 3.

Queues are commonly used in computer science and programming, especially in algorithms and data processing tasks. They can also be used in real-world scenarios, such as managing a line of people waiting to enter a venue or managing the delivery of items in a warehouse.