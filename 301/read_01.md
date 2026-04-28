# 301_Read_01

- [Component-Based Architecture](#component-based-architecture)
  - [Components](#components)
    - [Characteristics](#characteristics)
  - [Design Principles](#design-principles)
  - [Answers.1](#answers1)
- [Props in React](#props-in-react)
  - [What are React Props?](#what-are-react-props)
    - [How to Use](#how-to-use)
  - [Destructuring](#destructuring)
  - [Answers.2](#answers2)
- [Bookmark / Review](#bookmark--review)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This is important because...  
there is a easier, faster, more managable method of building sites and apps that can result in less errors.

## [Component-Based Architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

A method of segmenting a project into smaller, more manageable logical pieces. Component reusability is a vital part of component based architecture, as it combines functionality with repeated use cases (reduces time in development; increases reliability).  
Recognized standard component frameworks include, but not limited to; COM/DCOM, JavaBean, EJB, COBRA, .NET, web / grid services.

### Components

***The block.***  
Components are modular, replaceable, and reusable software objects that are constructed ahead of time with the intention of working with other components.  
Software components may be defined as a 'unit of composition'.  

Below is an example of a components structure, with a component being plugged inside.  
Note that the `Product` component must be imported first before being used. The syntax to invoke/plug the component becomes `<Product />`.  
`App` itself becomes a component we can later reuse and we allow this by opening the door through `export`.

```js
import Product from "./Product"

function App() {
  return (
      <div>
          <h1>PRODUCTS</h1>
          <div className="App">
              <Product />
          </div>
      </div>
  )
}

export default App
```

***Source***: [freeCodeCamp](https://www.freecodecamp.org/news/how-to-use-props-in-reactjs/#:~:text=parent%20component)

The three different views of a component are as follows; object-oriented view, conventional view, and process-related view.

**Object-oriented view**  
Multiple components working together as part of cooperating class(es). Problem domain and infrastructure class(es) (analysis, design; respectively), identify tributes and operations of the current implementation; interface definition that allow classes to communicate and cooperate.  

Components are self-managed, individuals; objects with their own logic and data; all interaction is done through the interface they define (methods/props).

**Conventional view**  
Components are seen as parts (elements, module, etc.) brought together and adapted to fit into something bigger; their encompassing logic, internal structure for logic to be processed, and interface that allows functionality and data processing.

More abstract take on components; they do their job however they see fit and we don't ask questions. Systems become easier to understand and maintain, because there is a separation of concerns and less micromanaging.

**Process-related view**  
Components are built from system library based on the context.  

Keeps the flow in mind, start-to-finish. Helps to understand flow of data and interactions, and can be critical for debugging and overall system design.

#### Characteristics

Reusability - designed to be re-used across situations / applications, but can be task-specific.
Replaceable - interchangeable with other similar components.
Extensible - functionality/structure can be expanded upon original scope.
Encapsulated - code block is contained within itself and rarely depend on other components.

### Design Principles

> "The design of data structures, interfaces, and algorithms should conform to well-established guidelines to help us avoid the introduction of errors."  - [tutorialspoint](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm#:~:text=The%20design%20of%20data%20structures%2C%20interfaces%2C%20and%20algorithms%20should%20conform%20to%20well%2Destablished%20guidelines%20to%20help%20us%20avoid%20the%20introduction%20of%20errors)

### Answers.1

1. What is a “component”?
    - (class) a small piece of code (javascript, html) that is reusable that produces UI elements; accepts input.
    - an interchangeable, re-usable block of code.
2. What are the characteristics of a component?
    - Independent / Contained (works on it's own)
    - Reusable
    - Scalable / Composable
    - Accepts input / manages state
    - Interchangeable
    - Expandable
3. What are the advantages of using component-based architecture?
    - (class) organization (cleaner code, maintanence), reusable (saves time, less errors, scalable).
    - reliable, easier development and deployment, reusable, maintainable and upgradeable.
(Optional). Disadvantages
    - May become complex managing many components.
    - Requires planning and design upfront.

## [Props in React](https://www.freecodecamp.org/news/how-to-use-props-in-reactjs/)

***Labels/data you attach to the block.***  
Props are objects and are used to pass data and values between components that return dynamic and unique outputs.  
When building with React, common occurrence for sites to have similar design patterns throughout their sections, only with different data, which is done through the use props, which build on the concept and use of components.

### What are React Props?

Props are inputs, methods of adding data into components, which they (components) can then use to expand upon the data they contain.  

#### How to Use

Data flow is one way, from parent component to child component. The child component also can not change or modify the data passed from the parent.  

To send props into a component, the syntax looks very similar to how attributes (class, id, etc.) are integrated to HTML elements.
The syntax to send props can look a little something like,  

```js
<Greeting name="you" age={1} />
```

and can have more than one property defined (name, age, etc.).  
Within the component receiving, we can now integrate the prop like so,  

```js
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

resulting in `Hello, you!`.

### Destructuring

A feature that allows the reassignment of data from objects or arrays to variables (think `Constructor` and how properties are defined in the initial parenthesis, only curly braces for this method). This method eliminates the need to use the `props.` prefix.

two different examples (within body, within parameters), in relation to our earlier example of `<Product />` are as follows;

```js
function Product = (props) => {
//First Step: Destructuring within the body of the function
    const { img, name, desc, price} = props ;
    return (
      <div>
          <img src={img} alt="products" />
//Second Step: receive the properties where you need them by stating the names of the properties without attaching the prefix ‘props.’
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}

export default Product
```

```js
//First Step: Destructuring within function's parameter
function Product = ({ img, name, desc, price}) => {
    return (
      <div>
          <img src={img} alt="products" />
//Second Step: receive the properties where you need them by stating the names of the properties without attaching the prefix ‘props.’
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}

export default Product
```

All this with the goal of making code more readable.

### Answers.2

1. What is “props” short for?
    - Properties
2. How are props used in React?
    - to pass data through components; from parent to child.
3. What is the flow of props?
    - one way, parent to child.

## Bookmark / Review

- ["Passing Data through Props" React Tutorial](https://reactjs.org/tutorial/tutorial.html)
- React Docs
  - [Hello World](https://reactjs.org/docs/hello-world.html)
  - [Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
    - Looks like HTML, but is JavaScript.
    - JSX is easier to read and allows cohesion of UI and logic.
    - ***The shape/design of the code block.***
    - A single parent element must be returned, `{}` is used to embed JS, and attribute use camelCase.
  - [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
    - ***The act of displaying React elements on page.***
    - React compares old UI vs. new and updates only what has changed, not everything.
  - [Components and Props](https://reactjs.org/docs/components-and-props.html)

## Things I Want To Know More About

- Object-oriented view
  - Conventional view
  - Process-related view
- When to use destructuring vs. `props.`.
