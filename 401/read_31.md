# 401_Read_30 - Context API

- [Choosing  State Structure](#choosing-state-structure)
  - [Answers](#answers1)
- [Passing State Deeply with Context](#passing-state-deeply-with-context)
  - [Answers.2](#answers2)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Choosing State Structure](https://react.dev/learn/choosing-the-state-structure)

As applications grow and components become more complex, maintaining the organization of state properly helps prevent bugs, unnecessary data duplication, and helps facilitate comms. between components.  

Aim to keep state simple with necessary info only, and reduce opportunities for inconsistencies and bugs.  

- **`State Structure`** - Organizing component data so it may stay consistent and easy to update.
- **`Context API`** - sharing information between compononets without passing props through every intermediate component.

### Answers.1

1. Five principles for structuring state.
    - Group related state - State variables that frequently chnage together should be combined into one variable / object to ensure they stay synched.
    - Avoid contradictions in state - Variables should be structure so that they do not resemble conflicting conditions.
    - Avoid redundant state - Don't store values that can already be calculated elsewhere through other state or props.
    - Avoid duplicating state - Maintaining a single source of truth vs. scattered copies of same info.
    - Avoid deeply nesting state - Aim for flatter structures; the deeper nested an object becomes, the more difficult to update and maintain.

## [Passing State Deeply with Context](https://react.dev/learn/passing-data-deeply-with-context)

Through the use of React's Context API, information is able to be shared across multiple components without the need to pass props through every level from pent to child. Enter `useContext`, alongside `createContext`, `eventHandlers`. Props are not going anywhere and should still be used. Reserve `useContext` for when data structure become too complicated for a did 

### Answers.2

1. What problem do **Contexts** aim to solve?
    - Prop drilling; which happens when data must be passed through multiple levels of components to reach where needed, even if intermediatary components do not need it.
    - Context allows parent components to provide data directly to descendant components that need it, regardless of how deeply nested.
2. What is one technique to try before `useContext`?
    - Pass props normally or simply restructuring to pass through children. This keeps data flow explicit.
3. What hook complements `useContext` for complex applications?
    - `useReducer` - manages complex state and updates logic.
      - `useContext` makes that state and update mechanism accessible to deeply nested components.

## Bookmark and Review

- [Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)
  - Lifting state to closest common parent. parent is truth and passes state, eventhandlers, etc. to children through props.
- [Preserving and Resetting State](https://react.dev/learn/preserving-and-resetting-state)
  - Preserving - React maintains tate when same component remains in same position of tree / file structure.
  - Resetting - State is reset when component is removed, replaced by defferent component type, etc.

- `useState` - Store and update component state
- `useContext` - Read shared data from a provider
  - `createContext` - Create the context
- `useReducer` - Manage more complex state logic

## Things to Learn More About

- context limitations
- resetting state
