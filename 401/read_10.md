# 401_Read_10 - Stacks and Queues

- [Stacks and Queues](#stacks)
  - [Stacks](#stacks)
  - [Queues](#queues)
  - [Conclusion](#conclusion)
- [Quiz](#quiz)
- [Big(O) Sheet](#big-o-cheat-sheet)

## [Stacks and Queues](https://gicw.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

Stacks and queues can both hold a collection of items, but they differ in the order items are allowed to leave. Same Items, Different Rules

### Stacks

As its name suggests, a **Stack** works like a stack of plates (or any other set of items that get *'stacked'* on top of the last). You add a plate to the top, and you must take the top plate off first.

```text
Top
[Plate C]  ← removed first
^
[Plate B]
^
[Plate A]  ← added first
```

This is called *Last In, First Out* (**LIFO**).  
The last item added is the first item removed.

The main operations all mainly deal with the top, or last item added; they are:

- `push(value)` — add an item to the top (+)
- `pop()` — remove and return the top item (-)
- `peek()` — view the top item without removing it (o-o)
- `isEmpty()` — check whether the stack has any items (?)

For example, in an empty array `[]`:

```text
push(A) → [A]
push(B) → [A, B]
push(C) → [A, B, C]

pop() → returns C
```

### Queues

A **Queue** works like a line at a store.  
New people join at the back, but the person who has waited the longest leaves first.

```text
Front                     Rear
[Alice] → [Ben] → [Carlos]
   ↑                       ↑
leaves first           joins here
```

This is called *First In, First Out* (**FIFO**).  
The first item added is the first item removed.

The main queue operations are:

- `enqueue(value)` — add an item to the rear (+)
- `dequeue()` — remove and return the item at the front (-)
- `peek()` — view the front item without removing it (o-o)
- `isEmpty()` — check whether the queue has any items (?)

For example, in an empty array `[]`:

```text
enqueue(Alice) → [Alice]
enqueue(Ben) → [Alice, Ben]
enqueue(Carlos) → [Alice, Ben, Carlos]

dequeue() → returns Alice
```

### Conclusion

The difference being, where items are removed:

|Structure|Add item|Remove item|Order|
|--|--|--|--|
|Stack|Top|Top|LIFO|
|Queue|Rear|Front|FIFO|

*Stacks* are useful when the most recent item should be handled first, (i.e. an Undo feature or the browser’s Back history).  
*Queues* are useful when items should be handled in arrival order, (i.e. customers waiting in line, or tasks waiting to be processed).

## Quiz

1. A stack uses _____ In, _____ Out order.
    <!-- LIFO -->
2. A queue uses _____ In, _____ Out order.
    <!-- FIFO -->
3. In a stack, which operation adds an item?
    <!-- `push()` -->
4. In a queue, which operation removes the next item?
    <!-- `dequeue()` -->
5. You add A, then B, then C to a stack. What does pop() return?
    <!-- C -->
6. You add A, then B, then C to a queue. What does dequeue() return?
    <!-- A -->
7. What is one real-world example of a stack?
    <!-- folding clothes, stacking boxes -->
8. What is one real-world example of a queue?
    <!-- necklace or a chain, song/movie queue -->
9. peek() lets you look at the next item without __________ it.
    <!-- performing an operation on it; removing it from structure -->
10. True or false: In a queue, new items join at the front.
    <!-- false -->

## Big O Cheat Sheet

|Operation|Stack|Queue|Big O|
|--|--|--|--|
|Add one item|`push()`|`enqueue()`|O(1)|
|Remove one item|`pop()`|`dequeue()`|O(1)|
|Look at next item|`peek()`|`peek()`|O(1)|
|Check if empty|`isEmpty()`|`isEmpty()`|O(1)|

Remember Big O here;  
O(1) means “one direct move.”

- Stack: go straight to top.
- Queue: go straight to front or rear.

Do not need to walk through every node/item first.

Direct pointer/reference?  → usually O(1)
Must walk through items?   → O(n)

Searching a stack or queue for a specific value would be O(n) because you may need to check every item.

### ✅ Discussion Checklist

Before you consider this assignment complete:

- [x] Read **Stacks and Queues**
- [x] Reply to the discussion by **teaching something you learned**
- [x] Review **one classmate's** post
- [x] Leave a **comment** on your classmate's post
