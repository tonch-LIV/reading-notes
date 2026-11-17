# 401_Read_30 - Hash Tables

- [Implementing Hash Tables](#implementating-hash-tables)
  - [Collisions](#collisions)
  - [Big(O)](#bigo)
  - [Quiz Review](#quiz-review)
- [Resources](#resources)
- [Things to Learn More About](#things-to-learn-more-about)

## Implementating Hash Tables

Hash tables are data structures that store info in **key-value** pairs, very similar to objects. A benefit is that they allow us to find info quickly without searcjing through every element.  

Hash tables work through the use of an **array**, the *hashing algorithm*, and '*buckets*' that organize info.  
The hashing function converts the key into an array `[index]`, from there, when you want to acces the value of the key; a hash function is calculated for the index.

### Collisions

Collisions is the term given when two completely different keys produce the same `[buckect index]`.  
**Separate chaining** offers a solution by allowing a linked-list to store multiple key-value pairs in the same bucket.  
**Open addressing** looks for another avilable slot within the array.  

### Big(O)

Hash tables provide **O(1) lookup time**. but this varies on the accumulation of collisions, where it can instantly change to **O(n)**.

**O(1)** - accesses the correct bucket, instantly. (Big benefit)  
**O(n)** - searches through many bucket.

### Quiz Review

1. What do hash tables store?
    <!-- - key-value pairs of data to quickly access. -->
2. What is the hash function and what does it do?
    <!-- - the hash function is the conversion between a *`key`* and a new `[index number]` so we know which bucket to access for the info being looked for. -->
3. A collision refers to what?
    <!-- - when multiple / different keys have the same index bucket number / hash. -->
4. What is the purpose of linked-list in regards to this reading and what we learned about buckets?
    <!-- - A linked-list is a way to circumvent the creation of collisions by allowing multiple pairs to be stored and searched inside one bucket. -->
5. What is the average Big(O) time lookup complexity?
    <!-- - O(1), constant -->

## Resources

- [Read Intro to Hash Tables](https://gicw.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- [Watch what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [Read basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
- [Skim hash table wiki](https://en.wikipedia.org/wiki/Hash_table)

## Things to Learn More About

- handling collisions - differences between separate chaining and open addressing.
- load impact - quantity of stored entries per bucket vs performance.
- table re-sizing - more or less buckets.
