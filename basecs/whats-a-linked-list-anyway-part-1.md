# What’s a Linked List, Anyway? [Part 1]

Original article: [What’s a Linked List, Anyway? [Part 1]](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

## Notes

Linked lists are a **linear data structure** meaning that there is a an order to how they are constructed and traversed.

The opposite of a linear data structure would be one that is not linear such as an object, or a tree.

Another example of a linear data structure would be an array.

Linked lists and arrays vary in how they use memory on our machines. When coding in a language like JS, or Python we don't have to worry as much about memory management since that is abstracted away.

Arrays are **static data structures**.

Linked Lists are **dynamic data structures**.

Meaning that when an array is created that stores 7 characters we would need 7 bytes of memory all in one place and if we were to add or remove from it we would need to recreate the array because the array would always need a given size or amount of memory.

Linked lists on the other hand don't need the memory to be stored sequentially and it can be scattered throughout and change dynamically.

### Parts of a Linked List

**head** - first node, only entry point to the list and all of the nodes.

**node** - element of the list that has the data and a pointer to the next element in the list.

**tail** - last node that points to null

A single node does not know about the length of the list or any other information outside of the data it contains and which node its pointer references. This is the reason that a linked list can be scattered thoughout memory because each node has a pointer or reference to the place in memory of the next node in the list.

### Different Linked Lists

**singly linked list** - starts at the head note, and points to the next node in a single direction until we reach the tail.

**doubly linked list** - each node contains two references, a reference to the next node and a reference to the previous node allowing us to traverse it in 2 directions.

**circular linked list** - the node that traditionally acts as a tail has a pointer to another node.
