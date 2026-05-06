# 301_Read_03

- [list and keys](#list-and-keys)
  - [Answers.1](#answers1)
- [The (money) Spread Operator](#the-money-spread-operator)
  - [Answers.2](#answers2)
- [Passing Functions to Children Components](#passing-functions-to-children-components---video)
  -[Answers.3](#answers3)
- [Bookmark / Review](#bookmark--review)
- [Things Id Like To Know More About](#things-id-like-to-know-more-about)

This is important because..

## [list and keys](https://react.dev/learn#rendering-lists)

### Answers.1

1. What does .map() return?
    - returns new array, does not affect original array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    - use `.map()` in JSX by turning array items into objects; `{}`.
3. Each list item needs a unique [____].
    - key
4. What is the purpose of a key?
    - keep track of each itme in a list.
    - Used to update / re-render efficiently based on identifying which items changed, rather than everything.

## [The (money) Spread Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

### Answers.2

1. What is the spread operator?
    - `...`, 'spreads' values from arrays/objects.
    - Helps to avoid mutating or changing the original data.
2. List 4 things that the spread operator can do.
    - Copy arrays.
    - Add items to arrays.
    - Combine arrays.
    - Merge Objects.
3. Give an example of using the spread operator to combine two arrays.

```js
const a = [1, 2];
const b = [3, 4];

const combined = [...a, ...b];
// [1, 2, 3, 4]
```

4. Give an example of using the spread operator to add a new item to an array.

```js
const b = [3, 4];
const b2 = [...b, 5, 6];
```

5. Give an example of using the spread operator to combine two objects into one.

```js
const obj1 = { name: "Antonio" };
const obj2 = { age: 25 };

const combined = { ...obj1, ...obj2 };
// { name: "Antonio", age: 25 }
```

## [Passing Functions to Children Components](https://www.youtube.com/watch?v=tqjn3DGbnT0) - video

### Answers.3

1. How do parent and child components share behavior in React?
    - Parent passes a function to the child through the use of props.
2. How are functions passed from a parent component to a child component?
    - through `.props`, like any other data.
3. How does a child component trigger a function that comes from its parent?
    - 

## Bookmark / Review

- ['Declaring Winner' tutorial](https://reactjs.org/tutorial/tutorial.html)
- [Lifting State up](https://react.dev/learn/sharing-state-between-components#lifting-state-up-by-example)

## Things Id Like To Know More About
