# 201_Read_07

- [Domain Modeling](#domain-modeling)
  - [Building a Domain Model](#building-a-domain-model)
  - [Answers.1](#answers1)
- [Table Basics](#table-basics)
  - [Creating a Table](#creating-a-table)
  - [Answers.2](#answers2)
- [Introducing Constructors](#introducing-constructors)
  - [Answers.3](#answers3)
- [Object Prototypes Using a Constructor](#object-prototypes-using-a-constructor)
  - [Functional Instantiation](#functional-instantiation)
    - [with Shared Methods](#with-shared-methods)
  - [Object.create](#objectcreate)
  - [Prototypal Instantiation](#prototypal-instantiation)
  - [Answers.4](#answers4)
- [Table Adv Features & Accessibility](#table-adv-features--accessibility)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This Topic Matters Because...  
Knowing how to properly structure code, through the use of HTML elements like `<table>` or JavaScript tools like `objects`, `constructor functions`, and/or `prototypes is vital to having a well written project that is not redundant where it does not need to be and is clearly legible and easy to follow.

## [Domain Modeling](https://www.thoughtworks.com/en-us/insights/blog/agile-project-management/domain-modeling-what-you-need-to-know-before-coding)

Concepts or objects which are interconnected with one another through behavior, vocabulary, etc. and are visually represented.

### Building a Domain Model

Through building a domain model, it aids in the creation process of a project by defining the encompassing entities/classes, as well as their associations between each other.  

**Entities** and/or **Classes** are anything and everything that is unique within the content and easily identifiable against others of its kind or of a different kind. What defines an entity/class can be as complicated or simple as it needs to be (i.e. apples to apples, or apples to oranges). Similarly, is their relationships with each other; entities can be of the same kind and related (apples == apples), may be related through association ((apples && oranges) == grow on trees), and so on for other associations.  
At a certain point, once enough detail is added in through attributes and properties, we migrate to a Class Diagram.

### Answers.1

1. Explain why we need domain modeling.
    - We need domain modeling to better understand what we are building and how we'll build the content within, in relation to each other and the structure as a whole.

## [Table Basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_table_basics#what_is_a_table)

A table is made of rows and columns, built to structure sets of data in a quick and easy to read manner.  
Accessibility tools also have the ability to access and interpret the data of tables when well implemented and structured.  
Tables also greatly benefit from styling! Stylistic choices allow the user to quickly discern between different data sets and categories.  
    - Links to table [css](https://github.com/mdn/learning-area/blob/main/html/tables/basic/minimal-table.css) and to HTML [template](https://github.com/mdn/learning-area/blob/main/html/tables/basic/blank-template.html).

Know when to use tables and when to not use them as they may hinder accessibility tools, increase markup tag creation and muddle html structure.

### Creating a Table

`<table>` and the closing `</table>` tags are the encompassing tags for table content.

- Cells are defined by the use of `<td>` (table data).
- Rows use the `<tr>` element and wrap around `<td>` elements to define table rows.
- Headers use the `<th>` element to define the start of rows or columns. Also wrapped around by `<tr>`.
  - headers are useful because, easier to differentiate between other simple cells/data.
  - use of the `scope` attribute allows headers to be associated with the data in corresponding row/column.
- `rowspan` and `colspan` attributes allow cells to span multiple units.
- By using the `<colgroup>` and `<col>`elements, we the developers are able to select/target columns and treat them as one.

### Answers.2

1. Why should tables not be used for page layouts?
    - For structuring data in an easy to see manner.
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.
    - Rows use the `<tr>` element and wrap around `<td>` elements to define table rows.
    - Headers use the `<th>` element to define the start of rows or columns. Also wrapped around by `<tr>`.
    - `rowspan` and `colspan` attributes allow cells to span multiple units.

## [Introducing Constructors](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#introducing_constructors)

A sort of template when using `object literals`; [read_06](201\read_06.md).

### Answers.3

1. What is a constructor and what are some advantages to using it?
    - a template for `object literals`; it defines the 'structure' of the `object` and can create new `property:value` pairs.
2. How does the term `this` differ when used in an object literal versus when used in a constructor?
    - "bind `this` to the new object, so you can refer to `this` in your constructor code".

## [Object Prototypes Using a Constructor](https://fireship.dev/beginners-guide-to-javascript-prototype)

### Functional Instantiation

When an `object` is built (as a function) with the future in mind to be re-used with differing values per key, this process of invoking the template to create a new `object` is referred to as `functional instantiation`; The function itself is a `constructor function`.

#### with Shared Methods

Instead of rebuilding/copy&paste methods used within the constructor for each new instance; the methods are moved to their own object and referenced by the other objects as needed. This prevents the wasting of memory and the existence of large objects.

### `Object.create`

A failsafe. `Object.create` - as it's name implies; allows the creation of an `object` that will refer to another `object`; should a lookup of an object fail.
In other words, if a call to an `object` key/value pair does not exist; `Object.create` will link it to am object that should have the corresponding data.  

```js
const uncleLeo = {
  bald: true,
  age: 35,
  likesFastCars: true
}

const me = Object.create(uncleLeo)
child.name = 'James'
child.age = 3

console.log(me.name) // James
console.log(me.age) // 3
console.log(me.heritage) // true
```

In this example, the `object` `me` does not contain the `key/value` pair which the `console.log()` function is calling for; however, `Object.create()` has essentially linked `me` to the `uncleLeo` object from which it may index the `likesFastCars` value and output `true` to the log.

Combining all three methods, Instantiation with Shared methods and Object.create, allows for cleaner code.

### Prototypal Instantiation

A common feature built in to javaScript, that deals with having to manage an entirely separate `object` in order to shared `method`s across different instances.  
A `prototype` property is something that every `function` in javaScript has, `object.prototype.method`.

The `new` keyword works in tandem with the `this` keyword during the creation of an `object`.

### Answers.4

1. Explain prototypes and inheritance via an analogy from your previous work experience.  
(NOTE: This is a very common front end developer interview question)
    - `prototypes` are a built in property into all functions that allows the sharing of methods across all instances of a function.
    - `inheritance` is moving up the ladder and being able to retrieve data that an object may not have.
    - Quite literally being left something as inheritance (besides money) that you can use to refence and answer questions. A family tree, historical record, employee manual, knowledge book/playbook

## Table Adv Features & Accessibility

A well built out table is easily interpreted by most* screen readers.  
In addition to column/row headers, there are many other elements that exist solely for marking up table content, such as:

- `<caption>` - nested within `<table>` and right after the opening tag for best placement. Provides a brief description regarding the contents of the table.
- `<thead>`, `<tbody>`, and `<tfoot>` - much like their non-table counterparts for an HTML document; provide structure to the build of the table. No visual enhancements and mainly useful when applying styling.
- `scope` - *covered up above*
- `id` / `headers` - attributes that function similarly to `scope` by creating associations between plain cells and header cells.

## Things I Want To Know More About

- Practicing building tables
  - `constructor`s and `prototype`s in action
