# How To Not Be Stumped By Trees

Original article: [How To Not Be Stumped By Trees](https://medium.com/basecs/how-to-not-be-stumped-by-trees-5f36208f68a7)

## Notes

Non-linear data structures do not follow an obvious numerical order like linked lists or arrays.

The fundamental difference between linear data structures and trees is that the root node of a tree can have links to multiple other nodes.

### Tree Common Terms

- **Root** - topmost node, never has links or edges connecting to it.

- **Link/Edge** - reference that a parent node contains that tells it what its child node is

- **Child** - node that has a parent that links to it.

- **Parent** - node that has a reference or a link to another node

- **Sibling** - any group of nodes that are children of the same parent node

- **Internal** - any node that has a child node

- **Leaf** - any node that does not have a child node in the tree

The data is hierarchical. Helpful to think of trees as a corporate ladder starting with a CEO, down to VPs, etc. or a family tree.

**n** nodes always means **n - 1** leaves/edges since the root node can never have a link to it.

Trees are recursive data structures meaning that they can contain other subtrees.

- **Depth** - the number of links or edges it takes to reach that node from the root node.

- **Height** - maximum number of links or edges (or the longest path from a node) to its furthest leaf.

Height/depth are important because they tell us a lot about the tree from the get go.

Trees can be balanced/unbalanced.

- **Balanced** - if any two sibling subtrees do not differ in height by more than one level.

- **Unbalanced** - if two sibling subtrees have more than one level of depth of difference.

A real life example of a tree is your computer's file system. You have a root directory with child nodes that could be subdirectories or subtrees of their own.
