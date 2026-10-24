# 401_Read_15 - binaryTrees

- [Trees](#trees)
  - [Defining / Analogy](#defining--analogy)
  - [Traversals](#traversals)
  - [Quiz](#quiz)
- [Things to Learn More About](#things-to-learn-more-about)

## [Trees](https://gicw.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

### Defining / Analogy

Think of binary trees similar to family trees.  
It's got your parents, grandparents, great-grandparents, and so on all the way down to the current generation, you.  

With some limitations and distinctions, the translation is *almost* 1-to-1.

- The **root** could be the furthest person depicted in the family tree.
- A **child** is any node/person with connection to a person before them (a **parent**).
  - (*NOTE: A Binary tree limits each node to two children max; called **left** and **right***)
  - A **leaf** is any node with a **parent** thay does not have any children themselves.  
- The **edge** is the connection between any two nodes/persons.

A rule is added through the use of Binary Search Tree; a node with a value less than its parent will go **left**, and larger than the parent, will go to the **right**.

### Traversals

The rule is expanded upon when referencing the traversal methods of;

|Method|Order|Memory trick|
|---|---|---|
|Pre-order|Root → Left → Right|Root first|
|In-order|Left → Root → Right|Root middle|
|Post-order|Left → Right → Root|Root last|

in an example, it would look like;  

|Method|Order|
|---|---|
|Pre-order|10 -> 5 -> 2 -> 7 -> 15 -> 12 -> 20|
|In-order|2 -> 5 -> 7 -> 10 -> 12 -> 15 -> 20|
|Post-order|2 -> 7 -> 5 -> 12 -> 20 -> 15 -> 10|

### Quiz

1. A node can have __ children.
    <!-- - 2; maximum, but also 1 or zero -->
2. Which traversal method wold return the values in ascending order?
    <!-- - in-order  -->
3. What are the 3 different traversal methods?
    <!-- - pre-order, in-order, post-order -->
4. Which traversal visits the root first?
    <!-- - pre-order -->
5. What's a good 'mental trick' to remember the different methods?
    <!-- - pre -> root first
    - in -> root middle (ascending)
    - post -> root last\
    - always left before right  -->
6. In an ideal scenario; what is the average time for a balanced BST in terms of Big(O)?
    <!-- - O(log(n)), allows the choice to ignore a branch depending on search parameters.  -->
7. What is the most likely scenario if every node must be visited?
    <!-- - O(n) -->
8. If a node does not have any 'progeny/children'; how is that node refered to?
    <!-- - leaf -->
9. Binary trees limit the number of children, but what is the data structure that doesn't limit that number called?
    <!-- - K-ary tree -->
10. Explain the difference between binaryTree and binarySearchTree?
    <!-- - Binary tree is the data structure the allows a node to have 2 children with no organization rule; a Binary search tree builds on the data structure by adding the rule of organizing smaller values on the left and larger values on the right as respective children to the parent node. -->
11. What is the first node in the tree called?
    <!-- - root -->
12. What is the difference between breadth-first and depth-first traversal methods?
    <!-- - Breadth-first traversal visits nodes one level at a time; meaning from root, children, then grandchildren; left to right (queue, FIFO). Whereas depth-first explores nodes and their branches before returning to other branches the same way (stack and recursive search). -->

## Things to Learn More About

- How a BST can got from O(log(n)) to O(n).
- Traversal order; pre (first) / in (middle) / post (last); left before right always.
