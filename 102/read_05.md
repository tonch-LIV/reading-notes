# 102_Read_05

- [CSS](#css)
  - [Adding CSS](#adding-css)
  - [Color](#color)
  - [Reference](#reference)
- [Myers Web Reset Stylesheet](#myers-web-reset-stylesheet)
- [Answer](#answer)

## CSS

**C**ascading **S**tyle **S**heet.  
Allows for control over how HTML elements are presented on a browser. Can change the color or size of text, or re-arrange the layout of a site, and even adding animations or backgrounds. This is achieved by defining rules that specify styles that should apply to elements or groups of elements, properties define values.  
i.e. element -> property(ies) -> value (example down below vv)  

If multiple / different style sheets have defined the same element(s) for different properties/values, then the last read (top to bottom) style sheet will be used. Inline styles having the highest priority since being the last read, external and internal fighting over precedence in the `<head>` element, and if all others fail, then browser defaults take precedence.

### Adding CSS

Three ways to incorporate CSS to an HTML doc.  
CSS can be directly applied within the HTML doc for a singularly unique HTML page by defining within the `<style>` element, within the `<head>`. element. Secondly, through an externally referenced .css file, linked within the `<head>` element. Lastly, by defining a singular element within a page by adding the style attribute to the desired element.

### Color

[Color](https://www.w3schools.com/colors/colors_picker.asp?colorhex=009B77) can be specified by name, hex value `#000000`, rgb value `rgb(0,0,0)`, or HSL(A) value `hsl(0,0,0,0)`.

### Reference

Any syntax error will invalidate the entire rule, which will then be ignored by the browser.

## Myers Web Reset Stylesheet

A reference to be used with the goal of reducing inconsistencies in commonly used elements across websites. "... a starting point... it should be tweaked, edited, extended, and otherwise tuned... "

## Answer

1. What is the purpose of CSS?
    - To personalize how sites are designed and presented on a browser.
2. What are the three ways to insert CSS into your project?
    - Internally referenced, linked externally, or inline.
3. Write an example of a CSS rule that would give all `<p>` elements red text.

``` CSS
p {
    color: red
}
```
