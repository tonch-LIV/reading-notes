# 201_Read_08

- [Learn CSS - Flexbox](#learn-css---flexbox)
- [CSS Layout - Flexbox](#css-layout---flexbox)
- [Learn CSS - Layout](#learn-css---layout)
- [Things I want to Know More About](#things-i-want-to-know-more-about)

This Topic Matters because...  

## [Learn CSS - Flexbox](https://web.dev/learn/css/flexbox/)

1. Flexbox is designed for one-dimensional content. Explain what this means.
    - Meant to be and best used for organizing and structuring a design layout for items of varying sizes and building a best placement for all those items. Organizes things one direction at a time;  main -> cross. but not both at a same time; for both, we would refer to grid.
2. Explain the difference between the main axis and cross axis.
    - "...  main axis is the one set by your flex-direction property." depending if the `property/value` is set to `row` or `column`, the value will affect items in a horizontal or vertical aspect, respectively.
3. How can using certain properties of flexbox negatively impact accessibility?
    - modifying content with properties that impact either visual order or logical order will impact the flow, as logical is the approach of many screen readers; screen readers parse by HTML order rather than visually how it's displayed. Testing should be doe to account for possible overlooked instances of accessibility mismanagement / misconfiguring.

## [CSS Layout - Flexbox](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Flexbox#flex-flow_shorthand)

1. What are some advantages of using flexbox over float?
    - vertical centering of content in relating to parentContainer.
    - children characteristics are shared (width x height) with no relation to parent available.
    - columns in a multiple-column layout adopt same height even if they contain a different amount of content.
2. How does this topic connect with your long term goals?
    - This topic aligns with long-term goal of and if, i were to work in a position that required attention and front house development and the what the client(s) engage with. Would allow me to better cater the needs and wants of the many who would interact with the program. Builds a foundation for learning CSS grid. It keeps layouts clean and easy to read.

## Learn CSS - Layout

## Things I want to Know More About
