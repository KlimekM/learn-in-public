# To Queue Or Not To Queue

Original article: [To Queue Or Not To Queue](https://medium.com/basecs/to-queue-or-not-to-queue-2653bcde5b04)

## Notes

Queue - linear abstract data structure that contains a long list of elements. Often referred to as FIFO (first-in-first-out). Functions similarly to an amusement park line where the first person to enter the line is the first person to exit the line.

Equeueing - the process of adding an element to the queue.

Dequeuing - the process of removing an element from the queue.

Array based implementations of a queue can be tricky if we don't know how large the queue will become so we need to copy over the contents, allocate more space and memory, and enqueue or add an item to the end of the array.

Space time complexity will grow when using an array because we will be adding/removing elements from opposite ends of the array.

Implementing a queue as a linked list becomes much simpler because we don't have to worry about the queue size since the memory is distributed and the queue can shrink/grow dynamically.

Once you remove the need to traverse the queue the space time complexity of enqueuing and dequeueing an element from the queue is constant of O(1).

Examples of a queue would be a server handling heavy load. It would queue requests as they come in simultaneously. Other examples would be job scheduling such as with Jenkins, the first job that is queued will run followed by the second, and so on as resources open up.
