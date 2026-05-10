# 301_Read_04

- [How to use Forms in React](#how-to-use-forms-in-react)
  - [Examples of forms and varying form elements](#examples-of-forms-and-varying-form-elements)
    - [login form](#a-simple-login-form-username-and-password)
    - [`onSubmit`](#use-of-onsubmit-to-tie-an-event-handler-to-button)
    - [uncontrolled form (`useRef()`)](#uncontrolled-forms-useref)
    - [Form Submission](#form-submission)
    - [Reset](#reset)
    - [Controlled Forms](#controlled-forms)
    - [Controlled vs Uncontrolled](#controlled-vs-uncontrolled)
    - [Dirty](#dirty)
    - [Validation](#validation)
    - [React Hook](#react-hook)
  - [Answers.1](#answers1)
- [The Conditional (Ternary) Operator Explained](#the-conditional-ternary-operator-explained)
  - [if ?](#if-)
  - [Ternary](#ternary)
  - [Answers.2](#answers2)
- [Bookmark and Review](#bookmark-and-review)
- [Things I'd Like to Know More About](#things-id-like-to-know-more-about)

This is important because...  
Forms produce state; state which can become a driver for UI. Ternary operators are a simplified way to express conditionals, but should be used in the right situations to avoid loss of legibility and other logic errors. Together, ternary operators can seamingly be implemented to dictate the output after a form is submitted.

## [How to use Forms in React](https://www.robinwieruch.de/react-form/)

Form creation in React involves managing it's state, the difference between controlled and uncontrolled forms (state and reference, respectively), submitting, reset, dirty fields, and validation; all things that can be implemented through the use of a form library.  

React uses `htmlFor` rather than `for` and it ties it to the matching `id`.

### Examples of forms and varying form elements

#### A **simple login form** (username and password)

```js
import * as React from 'react';

const LoginForm = () => {
  return (
    <form>

      <div>
        <label htmlFor="email">Email</label>
        <input id="email" type="text" />
      </div>

      <div>
        <label htmlFor="password">Password</label>
        <input id="password" type="password" />
      </div>

      <button>Submit</button>
    </form>
  );
};

export { LoginForm };
```

#### use of **`onSubmit`** to tie an event handler to button

```js
import * as React from 'react';

const LoginForm = () => {
  const handleSubmit = (event) => {
    event.preventDefault(); // function for action to occur when submitting
  };

  return ( // attribute for attaching eventhandler
    <form onSubmit={handleSubmit}>

      <div>
        <label htmlFor="email">Email</label>
        <input id="email" type="text" />
      </div>

      <div>
        <label htmlFor="password">Password</label>
        <input id="password" type="password" />
      </div>

      <!--`type=submit` tells the form to initiate the forms event handler-->
      <button type="submit">Submit</button> 
    </form>
  );
};

export { LoginForm };
```

#### **uncontrolled forms**

form values stored by browser, accessed only when needed through the use of references; `useRef()`.

```js
const emailRef = React.useRef(); // reference / save-state
// later on:
<input ref={emailRef} /> // input field that ties to the reference
// then to be read:
const email = emailRef.current.value; // variable in eventhandler function that updates save state
```

- `emailRef` is the object being referenced
- `.current`, the input element
- `.value`,  the user input

#### **Form Submission**

```js
const handleSubmit = (event) => {
  event.preventDefault();

  const email = emailRef.current.value;

  alert(email);
};
```

- `preventDefault()` prevents the page/browser default behavior of being refreshed when submitting.

#### Reset

React controls evrything centrally.  
No need to manually clear the DOM, target selectors for their value, or manipulate HTML.  

```js
const handleSubmit = (event) => {
  event.preventDefault();

  setForm({
    email: '',
    password: '',
  });
};
```

#### **Controlled Forms**

the preferred method when using React and forms

React state controls form values.  

`const [email, setEmail] = React.useState('');`  
`email` is the current value.  
`setEmail`, how the value will be updated.

Controlled forms are vital because they allow React to;

- know the current value,
- validate inputs,
- conditionally render UI,
- be able to disable buttons,
- show errors,
- reset fields easily.

Making controlled components the React standard.

#### Controlled vs Uncontrolled

Simple forms = uncontrolled; more intricate (use of state, multiple handlers) -> controlled.

#### Dirty

A change from the initial/pre-entered value.

#### Validation

A check on whether inputs are acceptable.  
(i.e. required inputs, password length, email or phone number format).

#### [React Hook](https://react-hook-form.com/)

Does not come with any form components, instead with custom React Hooks that allow for access to form, dirty, validation state and many others.

### Answers.1

1. What is a 'Controlled Component'?
    - The value of a form element which is controlled by React state rather than the browser.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    - asvp; at the moment it is being typed; allows React to know the current value, validate on the fly, produce live feedback, and conditionally render content.
    - React apps are built around real-time state updates.
3. How do we target what the user is entering if we have an event handler on an input field?
    - `event.target.value`
      - `event`, object created for changes in input.
      - `event.target`, element that triggered event.
      - `.value`, what is currently being input by user interaction.

## [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

Essentially shorthand for `if... else` statements.  
`? :`  

`let message = age >= 18 ? 'Adult' : 'Minor';`  

`:` separates the '`if`' (true) and '`else`' (false/otherwise), `?` after the condition.

### if ?

### Ternary

### Answers.2

1. Why would we use a ternary operator?
    - shorter syntax and cleaner legibility.
2. Rewrite the following statement using a ternary statement:

```js
if(x===y){
  console.log(true);
  } else {
  console.log(false);
  }
```

```js
x === y ? console.log(true) : console.log(false);
```

## Bookmark and Review

- [React Bootstrap - Forms](https://react-bootstrap.github.io/docs/forms/overview)
  - Bootstrap components are wrappers around HTML forms. Bootstrap impoves layout, styling, and consistency, without affecting the core form logic itself.
- [React Docs - conditional rendering](https://react.dev/learn/conditional-rendering)
  - Conditions, branching, render of different componenets based on state are examples of React UIs.  
  - Use of Ternary is ideal when the logic is short, expecting a return, JSX render is conditional.
  - `if... else` is better for when logic is drawn out and extensive.
  - nested conditions are in play.

## Things I'd Like to Know More About

- 