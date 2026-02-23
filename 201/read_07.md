# 201_Read_07

- [Domain Modeling](#domain-modeling)
  - [Building a Domain Model](#building-a-domain-model)
- [Table Basics](#table-basics)
  - [Creating a Table](#creating-a-table)
- [Introducing Constructors](#introducing-constructors)
- [Object Prototypes Using a Constructor](#object-prototypes-using-a-constructor)
- [Table Adv Features & Accessibility](#table-adv-features--accessibility)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This Topic Matters Because...

## [Domain Modeling](https://www.thoughtworks.com/en-us/insights/blog/agile-project-management/domain-modeling-what-you-need-to-know-before-coding)

Concepts or objects which are interconnected with one another through behavior, vocabulary, etc. and are visually represented.

### Building a Domain Model

Through building a domain model, it aids in the creation process of a project by defining the encompassing entities/classes, as well as their associations between each other.  

**Entities** and/or **Classes** are anything and everything that is unique within the content and easily identifiable against others of its kind or of a different kind. What defines an entity/class can be as complicated or simple as it needs to be (i.e. apples to apples, or apples to oranges). Similarly, is their relationships with each other; entities can be of the same kind and related (apples == apples), may be related through association ((apples && oranges) == grow on trees), and so on for other associations.  
At a certain point, once enough detail is added in through attributes and properties, we migrate to a Class Diagram.

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

1. Why should tables not be used for page layouts?
    - For structuring data in an easy to see manner.
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.
    - Rows use the `<tr>` element and wrap around `<td>` elements to define table rows.
    - Headers use the `<th>` element to define the start of rows or columns. Also wrapped around by `<tr>`.
    - `rowspan` and `colspan` attributes allow cells to span multiple units.

## Introducing Constructors

1. What is a constructor and what are some advantages to using it?
2. How does the term `this` differ when used in an object literal versus when used in a constructor?

## Object Prototypes Using a Constructor

1. Explain prototypes and inheritance via an analogy from your previous work experience. (NOTE: This is a very common front end developer interview question)

## Table Adv Features & Accessibility

## Things I Want To Know More About
