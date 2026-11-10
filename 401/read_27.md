# 401_Read_27 - useState() Hook

- [Thinking in React](#thinking-in-react)
  - [Summarize](#summarize)
- [State: A Component's Memory](#state-a-components-memory)
  - [Answers.2](#answers2)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Thinking in React](https://react.dev/learn/thinking-in-react)

Breaking the UI into smaller components, organizng a hierarchy, and determining where data should be managed is the ideal way of buidling a React app.  

Information in React typically flows from parent to child components through props in what is called **one-way data flow**.  

**Component hierarchy** is organizing components into parent-child relationships.  
Passing in formation between components is done through the use of **props**.  
**State** is what is called when information is stored that changes over time.  
When information / shared state is moved into a common parent component, that is known as **lifting state up**.  
An **inverse data flow** is when a child is allowed to request changes to parent state through the use of a callback function.  

### Summarize

In five steps the thinking in react;  

1. Break UI into hierarchy - Divide interface into smaller, reusable, components; organize according to relationship.
2. Build static version - Integrate components that render info as planned; no interactivity or state yet.
3. Build minimal & complete representation of UI state - ID what info will change over time, store in state;
4. ID where state will live - ID which components need access to state; locate closest common parent, when appropriate.
5. Add inverse data flow - allows child components to comm. user interactions back to parent through use of callback functions, state updates, and UI changes.

## [State: A Component’s Memory](https://react.dev/learn/state-a-components-memory)

As we know; React will re-render only the DOM elements which state has changed.  
How do components (unchanged) remember information between renders?  

Regular JS variables do not persist between renders and a change to their value, also does not trigger React to update them; so variables are not sufficient nor adequate for remembering information in this scenario.  

Enter `useState()`, which provides;  
State variable - stores the current value between renders.  
Setter function - updates state and requests re-render.

seen as,

```js
...
const = [state, setState] = useState();
...
```

**State is local to a component instance.**  
Two seperate instances of the same component can each maintain their own independant state.

### Answers.2

1. What is one reason a local variable isn’t sufficient for managing a React component?
    - Local variables don't persist through renders.
    - Updating the value of a variable, does not trigger React to re-render the componenent.
    - State variables do both
2. What is the argument to the `useState` hook, and what are the two parts of its return array?
    - argument is the **initial state value**.
    - returns an array with two elements,
      - current state variable stored.
      - setter function
3. How can Component A access state from Component B?
    - through lifting state up to the closest common parent
      - parent manages and passes down to A and B through props,
        - plus callback() so child can request updates to shared state.

## Bookmark and Review

Keep these pages handy - they answer questions that show up regularly for this lab.

- [Passing Props to a Component](https://react.dev/learn/passing-props-to-a-component)
  - passing from parent to child (data and functions).
- [Rendering Lists](https://react.dev/learn/rendering-lists)
  - use of `.map()`, `.filter()`, and unique keys to display collections.
- [State as Snapshot](https://react.dev/learn/state-as-a-snapshot)
  - state updates and time for values to change in current render.
- [useState hook](https://react.dev/reference/react/useState)
  - syntax, values, setter functions, and state updates.

## Things to Learn More About

- other 'unique keys',
- callback(),
- local state,
- deciding where state will live,
