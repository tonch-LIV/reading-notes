# 401_Read_05 - Linked List

## [Big O: Analysis of Algorithm Efficiency](https://gicw.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html) (Up through the section titled “Linear Complexity Growth”)

This reading centers around analyzing the efficiency of code / program execution through the size of the inputs, the measurements used, keeping the best and worst case situations in mind, and the differences between constant and linear growth.  
An algorithm's resource requirments can easily grow, whereas predicting the exact runtime is not an easy task wioth many variables to consider.

### Questions.1

1. What is the Big(O)? What does it measure?
    - <!--The Big(O) is the measure of how an algorithm's performance changes in relation to changes in the amount of data processed and resources needed.-->
    - <!--Time and Space complexity -->
2. What does `n` refer to?
    - <!--the input, specifically the size of the input; in a linked list, it would be the nodes.-->
3. What is the difference between Time and Space complexities?
    - <!--Time is not an exact measurement, rather how much work it will take -->
    - <!--Space referes to the amount of additonal memory that will be required. -->
4. What are the most commonly seen / used Big(O) metrics? Expand on how they work.
    - <!-- Linear, O(n) - work is relative to input size. i.e. linked list traversal / adding new node to the end. -->
    - <!-- Constant, O(1) - operation takes same amount of work (computation) regardless of input size. i.e. changing / adding a new head -->

## [Linked Lists](https://gicw.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html) + What’s a Linked List, Anyway [Pt.1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d) + [Pt.2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

A linear data structure (not unlike `arrays`, but different) built out of objects called `nodes`. Nodes re-direct to the next node in the Linked list until reaching the end of the list.

### Questions.2

1. What makes a list, a Linked List?
    - <!-- the objects in a Linked List all have direct, connected relationship; whether it be forwards or backwards. -->
2. What sets apart a Linked List from an Array?
    - <!-- there is now way to to access an item in a linked list like one would do with and array's index. it must got through the sequence. -->
3. In relation to Linked Lists; What is a 'Node'?
    - <!-- The name of the individual element inside the list; built as objects connected to one another. -->
    - <!-- `value` is the data stored in the node. -->
4. What is the significance of `Head` and the importance of `next` and `null`?
    - <!-- `Head` refers to the first node in the instance. -->
    - <!-- `next` points to the next node; at the end of the list, the last conection should be `null` (can still have a value). the first node should also be connected `this.next` to `null since it has niot been connected to another node *yet*. -->
5. What does 'Traversing a Linked List" mean? What is the process?
    - <!-- The act of visiting the nodes one at a time. Starting at the `Head`, reading its current value, following the `next` reference, repeating until `current` becomes `null` (end of list). -->
6. What is the 'Traversal Complexity' [Big(O)] for Linked Lists?
    - <!-- Time: O(n) because every node might be visited / relative to input size. -->
    - <!-- Space: O(1) because the function uses one current variable regardless of the list’s length.-->
7. Can new Nodes be added to a list? If, so, in which orientation? What changes about the traversal complexity?
    - _ <!--Yes; either beginning or end; beginning is O(1) - list is not traversed, end is O(n) - has to go through entire list (however big) to find final node -->
8. What is different between a 'singly', a 'doubly', and a 'circular' linked list?
    - <!-- a singly starts at the beginning, goes on towards the end, once there, it concludes. -->
    - <!-- a doubly can reference the preceeding node as well as the 'next' / sequential one. -->

## Things to Learn More About

- Big(o) changes within same function.
- circular linked lists
- where to use lists
