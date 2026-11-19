# 401_Read_30 - Context API - Behaviors

- [Scaling Up  witj Reducer and Contect](#scaling-up-with-reducer-and-context)
  - [Answers.1](#answers1)
- [Things to Learn More About](#things-to-learn-more-about)

## [Scaling Up with Reducer and Context](https://react.dev/learn/scaling-up-with-reducer-and-context)

As applications become larger and more complex, hooks such as `useReducer` and `useContext` help simplify state management.

Rather than having State update logic spread throughout various eventHandlers, the `useReducer` hook allows for organization of said State updates into a single reducer function.  
`useContext` on the other hand, allows components to access shared information ***without*** the need to repeadtedly pass props through various components throughout the file structure / the component tree, this helps avoid a problem known as **prop drilling**.

A dedicated Context provider component and **custom hooks** keep state mgmt. logic separate from other components that otherwise focus on UI or other aspects that would normally not need to interact with state.  

**`useReducer`** organizes ***how*** state changes.  
**`useContext`** simplifies **where** state can be accessed.  
Through the use of both, React apps are easier to organize, maintain, and expand upon.

### Answers.1

1. How do `useReducer` and `useContext` work together to simplify state management in a React application? (At least two paragraphs of prose.)

Rather than having state-changing logic scattered throughout different components throughout the file structure / directory; `useReducer` keeps the update logic in one place. `useReducer` handles state changes through a reducer function that determines how state should be updated based on dispatched actions.  

`useContext` further complements `useReducer` by allowing components to access shared state and the dispatch fucntion ***without*** having to have had them passed down through props. This avoids doing what is reffered to as **prop drilling**; reducing the number of components that interact with state where they otherwise would not need to. **Context providers** are used to hold both state and the dispatch function, thereby allowing components (that are within the scope of the provider) to retrieve info as needed and request updates.  

Together the `useReducer` and `useContext` hooks work together to make managing state in React apps more organized and efficient by separating state mgmt. from aspects like UI or the like; specially useful as applications grow.  

## Things to Learn More About

- `dispatch()` and `useReducer`: sending an action to reducer and managing state and how it changes.
- `createContext()` and `useContext`: sharing information and allowing descendants to access context.
- 