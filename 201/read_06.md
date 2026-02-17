# 201_Read_06

- [JavaScript Object Basics](#javascript-object-basics)
  - [Object Basics](#object-basics)
  - [Dot notation](#dot-notation)
  - [Bracket Notation](#bracket-notation)
  - [Object Members](#object-members)
  - [What is "this"?](#what-is-this)
  - [Constructors Intro](#constructors-intro)
  - [It's Been Objects all along](#its-been-objects-all-along)
  - [Answers.1](#answers1)
- [Intro to the DOM](#intro-to-the-dom)
  - [Answers.2](#answers2)
- [Save & Review](#save--review)
  - [Problem Domain](#problem-domain)
  - [Primitive Values & Object References](#primitive-values--object-references)

This topic maters because...  
Through the use of DOM; we, the developers are able to manipulate elements and add more dynamic elements to our site/document. Knowing what DOM entails and how to incorporate it into existing projects is vital to using it.

## [JavaScript Object Basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#object_basics)

### Object Basics

Much like an `array`, an `object` is a collection of related data. Objects can house multiple variables and/or functions, which change names to properties and methods, respectively, when found inside objects.

Objects syntax is not all that different from what we've been using from variables/arrays; we define the name of the object (whether `let` or `const`), then curly braces `{}` house the data. Once inside, its much like CSS syntax, `members` on the left, separated by a colon `:`, then `values` on the right; each name-value pair being separated by a comma `,`.

```js
const objectName = {
  member1Name: member1Value,
  member2Name: member2Value,
  member3Name: member3Value,
};
```

Data types include, but not limited to; functions (methods), and arrays and numbers (properties).  

**Object Literal** - when a function inside of an object omits the keyword (function) in its definition/declaration.

### Dot notation

`objectName.item` is the syntax used to access properties or methods within an object. The preferred method. Nesting an object within an object is also valid syntax.

```js
let objectName = {
  propertyObject: {
  property: value
    }
}
```

The syntax would just be expanded upon, adding the nested object name to the chain. `objectName.propertyObject.property;`. Be sure to properly update any necessary invocations.

### Bracket Notation

Much like Dot notation and visually similar to syntax for an array; is a method to invoke an objects properties. Using the previous sample code, it would look something like, `objectName["propertObject"]["property"]`. Mostly usable for trying to access an object property contained within a variable; dot notation would not work for this.

### Object Members

You are able to update the value(s) of an object property through the use of the assignment operator, `objectName["property"] = "newValue";` or `objectName.property = newValue;` and similarly to create new properties also.

### What is "this"?

`this` is a keyword to specify upon the current object which the code should reference to execute code. Allowing the same definition to work across multiple objects.

### Constructors Intro

Essentially a template for object literals with the ability to create new objects in the future.

```js
function objectName(property1, property2) {
  this.property1 = value1;
  this.property2 = value2;
}
```

and to create/add new objects we would use the keyword `new`, like so;

```js
const variable1 = new objectName2(value1, value2);
const variable2 = new objectName2(value1, value2);
```

### It's Been Objects all along

Objects are an integral part to javascript and very prominent when using APIs.

`Array`  
`Math`  
`String`  
`Document`  

Although, not all create object instances, and may require instantiation.

### Answers.1

1. How would you describe an object to a non-technical friend you grew up with?
    - Objects hold data, related to specific topic or subject.
2. What are some advantages to creating object literals?
    - shorter syntax, more data consolidated together, efficient when wanting to identify individual items by name.
3. How do objects differ from arrays?
    - we access by property, rather than index number.
4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
    - when value is held within a variable, not accessible through dot notation.
5. Evaluate the code below. What does the term this refer to and what is the advantage to using this?
    - In this specific snippet, `this.` refers to `dog`. reusable and adaptable per object used in.

```js
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
}
```

## [Intro to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)

**Document Object Model**  

### Concepts and Usage

Uses the structure of a document to connect to scripts and/or programming languages, through the use of the objects derived from the document.  
Objects are derived from nodes, which in turn are derived from branches. Using DOM, we are able to access parts of the tree to modify structure, style, or content as needed.

DOM is a collection of various APIs working together. The DOM tree is a visual representation of how the document is viewed, parsed, then displayed.  
Without DOM, javaScript would not know what to do with documents, since DOM is used to access the document and its elements.

DOM is a web API, independent, not integrated into anyone language, thus can be built for any language.

By using the inline `<script>` tag or other means for using javascript, you are automatically and immediately using the DOM.

### DOM Interfaces

[List](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model#dom_interfaces) of interfaces defined in DOM specs.

Node is an all-encompassing term, as every object is a node of some sort or another.

### [HTML DOM](https://developer.mozilla.org/en-US/docs/Web/API/HTML_DOM_API)

A `Document` interface refers to a document containing HTML, then extended upon by HTML-specific features.

### [SVG DOM](https://developer.mozilla.org/en-US/docs/Web/API/SVG_API)

Also falls under `Document` interface, under SVG specific features.

### Answers.2

1. What is the DOM?
    - Document Object Model, A collection of APIs used to access and manipulate the structure and elements therein.
2. Briefly describe the relationship between the DOM and JavaScript.
    - JavaScript uses DOM to access and manipulate the structure and elements.

## Save & Review

### Problem Domain

### Primitive Values & Object References

## Things I Want To Know More About

- Building function using the DOM
