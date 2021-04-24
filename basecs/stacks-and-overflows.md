# Stacks and Overflows

Original article: [Stacks and Overflows](https://medium.com/basecs/stacks-and-overflows-dbcf7854dc67)

## Notes

A stack is a linear data structure. If we want to add or remove items from it we can only do so from the top.

An analogy for a stack would be a stack of plates or a stack of books.

Stacks are often refered to as LIFO (last in, first out). The other common abbreviation is FIFO (first in, first out) which referes to a queue and is synonymous with an amusement park line.

Stacks are often implemented as a singly linked list since items can added/removed from a single place.

Adding or removing elements from the beginning of a linked list happens at a space time complexity of O(1) or constant time so no matter how large the stack gets the addition or removal of an item from the stack can happen rather quickly.

Stacks can also be implemented as arrays but arrays are static data structures that require a set amount of memory. Stacks can grow infinitely large though and when they grow past the size allocated for the array that leads to a stack overflow.

Implementing a stack is rather easy, but there are a few functions that will always be needed.

- push - add item onto the top
- pop - remove item from the top
- top(peek) - check the value of the item at the top without removing it.
- isEmpty - function to check if the stack is empty
- size - function that checks how many elements are in the stack

#### Examples of stacks in real life

- a text editor's undo/redo functionaliy.
- a browser's history
- a call stack
