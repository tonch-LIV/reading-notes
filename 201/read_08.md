# 201_Read_08

- [Learn CSS - Flexbox](#learn-css---flexbox)
        - [Main Axis and Cross Axis](#main-axis-and-cross-axis)
        - [Flex Container](#flex-container)
            - [Controlling Direction Inside](#controlling-direction-inside)
            - [Wrapping Items](#wrapping-items)
            - [Controlling Space Inside Item](#controlling-space-inside-item)
            - [Item Reorder](#item-reorder)
        - [Alignment Overview](#alignment-overview)
            - [Space Distribution on Main](#space-distribution-on-main)
            - [Distribution on Cross](#distribution-on-cross)
            - [Alignment on Cross Axis](#alignment-on-cross-axis)
        - [Answers.1](#answers1)
- [CSS Layout - Flexbox](#css-layout---flexbox)
        - [Flex Boxes](#flex-boxes)
            - [To Column or To Row?](#to-column-or-to-row)
            - [Wrapped](#wrapped)
            - [flex-flow Shorthand](#flex-flow-shorthand)
        - [Sizing Flex items](#short-vs-long)
            - [Short vs Long](#short-vs-long)
        - [Horizontal vs Vertical Alignment](#horizontal-vs-vertical-alignment)
        - [Item Order](#item-order)
        - [Nesting the Flex](#nesting-the-flex)
        - [Answers.2](#answers2)
- [Learn CSS - Layout](#learn-css---layout)
- [Things I want to Know More About](#things-i-want-to-know-more-about)

This Topic Matters because...  

## [Learn CSS - Flexbox](https://web.dev/learn/css/flexbox/)

A layout model intended to be used for one dimensional content; for creating an optimal layout for items of varying sizes by providing flexible boundaries of display.  

- Through flexbox, the developer has the ability to display items as a row (horizontally) or a column (vertically), and aligning them within either.  
- Items in a flex container are single line / grouped `inline` by default, but may extend or `wrap` to additional lines.  
- Items can become "bigger" by distributing space inside the item, in relation to the space or their parent element container.  
- The items will respect the writing mode / logical order of the document, even when re-ordered differently visually.

### Main Axis and Cross Axis

Both main axis and cross axis direction will be determined by the value of the `flex-direction` property.  

- When set to `row`, the main axis goes horizontal, left-to-right; at this time, the cross axis will default to vertical, up-and-down.  
- When `flex-direction` is set to `column`, the main axis will be vertical, top-to-bottom, and the cross axis will go left-to-right.  

### Flex Container

To create a "flex container", we specify the `display` property of the parent container as `flex`. By doing this, we essentially open up the accompanying `property: value` rules to modify the layout.

The initial / default values (nothing else specified, but `display: flex`) entail that items will display as a row (horizontally), will NOT wrap, will not change in in size within their container, and their fixed positioning will be at the start of the container (top-left).

#### Controlling Direction Inside

Items inside the container reference the main axis and move as a group. However, items can be moved individually or as a group, in relation to the cross axis.  

To begin modifying the orientation or flow of items, we create a new property of `flex-direction`. `row` being the default setting, does not need to be specified, but changing the value to `column` will change the way the items arrange themselves from horizontal to vertical.

We can append `reverse` to either `row` or `column` and the order will change to being displayed backwards (think 1, 2, 3, 4 to 4, 3, 2, 1). This should be done carefully as it affects accessibility tools such as screen readers or navigating content through the keyboard; which operate of the logical order, not visual.

#### Wrapping Items

Default value for `flex-wrap` is `nowrap`, meaning that items that do not fit within the confines of a resized parent container will 'overflow' / disappear from view. This is remedied by changing the value to `wrap`; although items will move to 'a new line' below the first item(s) that fit, but remain relative to their `flex-direction` setting. This is known as creating multiple **flex-lines**.

`flex-flow` is a shorthand property that controls both `flex-direction` and `flex-flow`, followed by the values you so desire.

#### Controlling Space Inside Item

Like mentioned before; the default starting position of items with solely `flex-direction` is at the top left, if items do not occupy the entirety of the available space, they remain fixed, they do not grow to fill the void. They respect their content sizes.  

This can be modified with a rule `flex-grow` or `flex-shrink`; values of `0` means they do not change, `1` means they grow or shrink, respectively. `flex-basis: auto` indicates item in their natural dimensions.  

`flex-auto` will force items to disregard their individual sizes and make them a consistent size.

#### Item Reorder

The `order` property allows items to be rearranged from their natural order, dictated by the `flex-direction` property.  
***(\*Using this property leads to similar problems as `row-reverse` and `column-reverse` and should not be used as a quick fix rather than being fixed by editing the HTML file!)***

### Alignment Overview

**The following properties for aligning items and distributing space between items are shared with the Grid Layout as well.**

#### Space Distribution on Main

Properties begin with `justify` on main.  

- `justify-content` - initial value is `flex-start`. Items placed on left/start of container, with any empty space not occupied by items on the right.
        - `flex-end` - items placed on the right/end of container.
        - `space-between` - distributes space evenly between items and edges of container (think margin walls).

When working with the `flex-direction` of `column`, add `height` or `block-size` to ensure there is plenty of space to distribute for items.

#### Distribution on Cross

Properties begin with `align`.  

- `align-content` - uses same values as `justify-content`. Although, initial value is `stretch` rather than `flex-start`.
        - don't forget about `height` or `block-size`.

(**`place-content`** - a shorthand for both `justify` and `align` with either one or two values. Single value will apply to both axes; otherwise it's `align-content`, then `justify-content`.)

#### Alignment on Cross Axis

Space available for alignment will depend on height of container, or flex line in case of wrapped items.

- `align-self` - for a single item; same initial value, `stretch`. property is added to items rather than container.
- `align-item` - aligns all items as a group and should be added to container.

- Other values include,
        - `flex-start`
        - `flex-end`
        - `center`
        - `stretch`
        - `baseline`

**To achieve centering of items in a container vertically and horizontally, a simple combination of `justify-content: center` and `align-items: center` will take care of that.**

### Answers.1

1. Flexbox is designed for one-dimensional content. Explain what this means.
    - Meant to be and best used for organizing and structuring a design layout for items of varying sizes and building a best placement for all those items on a website horixontally and vertically.
2. Explain the difference between the main axis and cross axis.
    - Does not change, what changes is our perception / the structuring of the container. When `flex-direction` is set to `row`(default), the main axis is horixontal / left-to-right. When set to `column`, the main axis is vertical / top-to-bottom.
3. How can using certain properties of flexbox negatively impact accessibility?
    - modifying content with `property: value` pairs that impact either visual order or logical order will impact the flow, as logical is the approach of many screen readers. Testing should be done to account for possible overlooked instances of accessibility mismanagement / misconfiguring.

## [CSS Layout - Flexbox](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Flexbox)

Called `flex`, because items expand (or shrink) to fill / accommodate space given.  
It is used for centering relative to the parent, equally distributing space available to the children elements, among other finite detailing around the layout.

### Flex Boxes

We enable flexbox to the parent element, so that the children will receive the effects of the rules applied.  
The main rule is `display: flex`. The container / parent element is now operating as a pseudo block level element in relation to how other elements and itself behave with each other. Although, we could append `inline` to the `flex` value and have it behave as an inline element.. The items within are called flex items.  

#### To Column or To Row?

The `flex-direction` is the property that dictates the flow / direction the main axis runs along. The value `row` reads left-to-right and `column` goes top-to-bottom.

#### Wrapped

Children that exceed the dimensions of the parent overflow, that is to say that they continue past the intended viewport. The `flex-wrap: wrap` rule is intended to remedy this situation and 'move' overflowed items down onto a new line.

#### flex-flow Shorthand

Meant to be utilized as a combination / replacement ruleset for `direction` and `wrap`, `flex-flow` will structure both with either one or two values; one for both or two for `direction` and `wrap` respectively.

### Sizing Flex items

- The `flex` property dictates how much space that is available each child / flex item will occupy in relations to the other items.
        - `1` - a value that will each divide the space evenly after considering margin and padding.

#### Short vs Long

Using the `flex` shorthand we combine the use of three different properties; `flex-grow`, `flex-shrink`, and `flex-basis`.

### Horizontal vs Vertical Alignment

- `align-items: center` to center based on the cross axis.
        - `normal` is the default (`stretch`). stretches items to fill parent container in direction set by `flex-direction`
        - `center` will allow the items to keep their respective dimensions and center along cross axis.
- `align-self`: applys and overrides for individual items.  

- `justify-content: space-around` to space the items evenly throughout the main axis.
        - `normal` is also default (`start`). items will sit at beginning of main axis.
        - `end` / `flex-end` will position them at the end of the main axis.
        - `center` is also a valid alternative for `justify-content`; positions items at center of main axis.
        - `space-between` is very similar to `space-around` other that it puts items at the very edge, to the border of the parent container.

### Item Order

We are able to manipulate the order of items from their natural, logical order using the `order` property; the default is `0`.  
The lower the order value, the sooner it will appear visually / get moved forward

### Nesting the Flex

Very much valid to specify children of a container, as parent for other elements.

### Answers.2

1. What are some advantages of using flexbox over float?
    - vertical centering of content in relating to parentContainer.
    - children characteristics are shared (width x height) with no relation to parent available.
    - columns in a multiple-column layout adopt same height even if they contain a different amount of content.
2. How does this topic connect with your long term goals?
    - This topic aligns with long-term goal of and if, i were to work in a position that required attention and front house development and the what the client(s) engage with. Would allow me to better cater the needs and wants of the many who would interact with the program. Builds a foundation for learning CSS grid. It keeps layouts clean and easy to read.

## Learn CSS - Layout

## Things I want to Know More About
