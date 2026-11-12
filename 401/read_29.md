# 401_Read_29 - Advanced State with Reducers

- [Extracting State Logic into a Reducer](#extracting-state-logic-into-a-reducer)
  - [Answers.1](#answers1)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)

Components may become 'hard to read' while employing `useState()`, and having multiple eventHandlers that each contain their own logic to update state.  
In such situations, React recommends a *reducer* (`useReducer()`), which gathers said updates into one predictable location , rather than each eventHandler directly calculating the next state.  
The handler describes *what happened* through an action, the **reducer** decides *how the state should change*, accordingly.

A reducer is a function that receives two parameters; the **current state**, and an **action**, with a *return* of the **next state** for the next render (of the same state throughout, whithout side effects).

Going from `useState()` -> `useReducer()` in,  

1. dispatch actions from `eventHandlers()`
2. write reducer that handles actions
3. replace original `useState()` with `useReducer()`

or,  

```text
Event happens -> action dispatched -> reducer recieves state + action -> reducer returns new state -> React re-renders
```

### Answers.1

1. What is the motivation for adding a reducer?
    - to organize state management,
    - improve legibility,
    - gather state update logic into one function,
    - facilitate troubleshooting
2. What are actions in the context of a reducer?
    - an object sent to reducer, describing something (event) that happened in app.
    - usually contains `{type: ""}` property that'll describe the event & may have additional info needed to process.
3. How are actions different than setting state directly?
    - with `useState()`, event handler states specifically how to change,
    - with reducer, event handler describes the change through object properties while actual state-update logic is held in reducer and let reducer decide how to change
4. What common list operation is `useReducer()` named for, and why?
    - array method, `array.reduce()`
    - takes 'result-so-far' and next item to produce new result; same concept,
    - current state + action -> next state
5. When should you switch from useState to `useReducer()`?
    - `useReducer()` is useful when dealing with many eventHandlers updating the same state.
    - to help with future troubleshooting.
    - to organize scattered state-update eventHandlers.

## Bookmark and Review

- [useReducer hook](https://react.dev/reference/react/useReducer)
  - dispatch of action, reducer calculates value.
- [Keeping Components Pure](https://react.dev/learn/keeping-components-pure)
  - Components and reducers expected to behave like pure functions,
  - Props, state, etc. should be treated as read-only,
  - renders should not modify outside variables or objects.
  - pure reducers allow state changes to be more predictable and easier to debug.
  - strict mode.
- [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)
  - state updates can be batched and processed after eventHandler finishes; elimiating unnecessary, halfway re-renders.

## Things to Learn More About

- Pure reducers - calculating state only; side effects elsewhere.
- Immutable state - returning new arrays/objects.
- useState vs useReducer use case.
