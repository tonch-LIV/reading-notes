# 301_Read_03

- [list and keys](#list-and-keys)
  - [Answers.1](#answers1)
- [The (money) Spread Operator](#the-money-spread-operator)
  - [Answers.2](#answers2)
- [Passing Functions to Children Components](#passing-functions-to-children-components---video)
  -[Answers.3](#answers3)
- [Bookmark / Review](#bookmark--review)
- [Things Id Like To Know More About](#things-id-like-to-know-more-about)

This is important because...
knowing different things you can do within react components allows for a better user interface and ultimately a better experience.

## [list and keys](https://react.dev/learn#rendering-lists)

We rely on `for` loops and `.map()` in order to render lists.  
`key` attributes gives the array set some structure by identifying and tagging the data with a unique identifiers.  

**example:** an array of vehicles

```js
const vehicles = [
  { title: 'Car', id: 1 },
  { title: 'Bus', id: 2 },
  { title: 'Truck', id: 3 },
];
```

The `map()` function is then used within the component to transform the array into usable list items.

```js
const listItems = vehicles.map(product =>
  <li key={vehicles.id}> // key tied to and pulling from the id value
    {vehicles.title}
  </li>
);

return (
  <ul>{listItems}</ul>
);
```

`key` is used as an attribute for `<li>`; unique identifier for item within the array.  
*'React uses your keys to know what happened if you later insert, delete, or reorder the items.'*

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

Allows expansion (or copying) of elements (for arrays), arguments (for function calls), and/or strings.  
Properties of an object are enumerated (contents returned) in an object literal; adds key value pairs to created object; Not all objects are iterable.  

Spread is used when created a new array or object and would like to include original elements from original array/object.  
Also able to be used in function arguments.

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

Functions are passed down as props, within Components to share behavior 'down the ladder'.

### Answers.3

1. How do parent and child components share behavior in React?
    - Parent passes a function to the child through the use of props.
2. How are functions passed from a parent component to a child component?
    - through `.props`, like any other data.
3. How does a child component trigger a function that comes from its parent?
    - through an eventlistener or some other capturable action registered through the child.

## Bookmark / Review

- ['Declaring Winner' tutorial](https://react.dev/learn/tutorial-tic-tac-toe)
- [Lifting State up](https://react.dev/learn/sharing-state-between-components#lifting-state-up-by-example)
  - When multiple Components need the same data, allocate state to the common parent.

## Things Id Like To Know More About

- practice with passing fucntions as props.
  - creation of lists thrpugh map() and getting familiar with keys.
