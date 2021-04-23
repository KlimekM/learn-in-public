# What’s a Linked List, Anyway? [Part 2]

Original article: [What’s a Linked List, Anyway? [Part 2]](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

## Notes

Big O Notation is a way of evaluating
the performance of an algorithm.

One way to think about Big O is
a way to express how long a function, or algorithm takes to run based on how many elements we pass to the function.

Lots of equations to determine the space and time complexity of an algorithm, most involve an **O** (sometimes referred to as order) and a variable **n** where n is the size of the input, hundreds, thousands, etc.

When looking at a Big O chart, the time or the operations (O) are on the y-axis. The input size, space, or the n is on the x-axis.

Example chart:
![Big O Graph](https://miro.medium.com/max/1400/1*yiyfZodqXNwMouC0-B0Wlg.png)

In terms of linked lists the two
Big O equations to remember are O(1) and O(n).

**O(1)** - takes constant time, does not matter how many elements we have or how big the input is because it will always take the same amount of time and memory to run the algorithm.

**O(n)** - linear, as our input grows the space (y axis) and time (x axis) needed to run the algorithm grows linearly.

**O(n<sup>2</sup>)** - exponentially grows and uses more time/memory as the number of elements that we have increases.

### Growing a Linked List

We can add or remove elements from a linked list without allocating memory in advance or recreating our linked list. All we need to do is rearrange the pointers.

If we want to insert a node at the beginning of a linked list.

- We would need to find the head node.
- Create a new node, and set the pointer to the current first node in the list.
- Rearrange the head node's pointer to point at the new node.

The above steps must be done in order, because flipping step 2/3 could end up with a cyclical structure with only two nodes.

Inserting an element at the beginning of a list takes the same amount of time no matter how long the list is. Hence the operation is **O(1)** or constant.

Inserting an element at the end of the list is a different story and the Big O would be **O(n)**. We would still take the same steps, but would have to traverse through the entire linked list to find the last node which would take longer if there were 1,000,000 elements vs 10.

General rule of thumb:

- a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.

Indexing or traversal is much easier in an array that takes up a single chunk of allocated memory and you can use an index vs. traversing through each element at a different address in memory doing so with a linked list.

## Notes from Additional Sources

[A Beginner's Guide to Big O Notation](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation)

**O(1)** - constant

Example:

```ts
function isFirstElementNull(elements: string[]): boolean {
  return elements[0] === null;
}
```

**O(n)** - linear, needs to loop through every element until entry is found.

```ts
function includesValue(elements: string[], value: string): boolean {
  if (elements.includes(value)) {
    return true;
  }

  return false;
}
```

**O(n<sup>2</sup>)** - performance proportional to the square of the size of the input set, a loop within a loop would be **O(n<sup>2</sup>)**. Deeper nested iterations would grow to **O(n<sup>3</sup>)**, **O(n<sup>4</sup>)**, etc.

**O(2<sup>^</sup>n)** - denotes an algorithm whose growth doubles with each addition to the input data set. The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. An example of an O(2^N) function is the recursive calculation of Fibonacci numbers.

```ts
function fibonacci(num: number): number {
  if (num <= 1) {
    return 1;
  }

  return fibonacci(num - 1) + fibonacci(num - 2);
}
```

**O(log n)** - Binary search is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match, it will return success. If the target value is higher than the value of the probe element, it will take the upper half of the data set and perform the same operation against it. Likewise, if the target value is lower than the value of the probe element, it will perform the operation against the lower half. It will continue to halve the data set with each iteration until the value has been found or until it can no longer split the data set. This is extremely efficient when dealing with large data sets.
