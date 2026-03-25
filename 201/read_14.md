# 201_Read_14

- [CSS Transforms](#css-transforms)
  - [2D Transforms](#2d-transforms)
  - [Combining Transforms](#combining-transforms)
  - [Transform Origin](#transform-origin)
  - [3D Transforms](#3d-transforms)
  - [Answers.1](#answers1)
- [CSS Transitions & Animations](#css-transitions--animations)
  - [Transitions](#transitions)
    - [Properties](#properties)
    - [Duration](#duration)
    - [Timing](#timing)
    - [Delay](#delay)
  - [Animations](#animations)
  - [Answers.2](#answers2)
- [Simple, Grand CSS3 Transitions](#simple-grand-css3-transitions)
  - [Answers.3](#answers3)
- [Psychological Safety](#psychological-safety)
  - [Lessons From Google](#lessons-from-google)
- [Bookmark/Skim](#bookmarkskim)
  - [Pure CSS Bounce](#pure-css-bounce)
  - [Buttons Animated](#buttons-animated)
  - [CSS3 Animations: Keyframes](#css3-animations-keyframes)
  - [404](#404)

This is important because...  
Being able to add dynamic visuals to engage the users attention leads to a favorable experience to them. Done tastefully also... and when called for / where it fits.

## [CSS Transforms](http://learn.shayhowe.com/advanced-html-css/css-transforms/)

Allows new and different ways to size, position, and change elements in either 2D or 3D settings (with individual properties and values) thanks to CSS3 update.  

Syntax is pretty straight forward; `transform` property keyword, followed by the transform type and then the amount in parenthesis, occasionally and to offer best support across browsers, one may include vendor prefixes.

```css
div {
  -webkit-transform: scale(1.5);
  -moz-transform: scale(1.5);
  transform: scale(1.5);
}
```

### 2D Transforms

Works on the `x` (horizontal) and `y` (vertical) axes.  

- `rotate` as a value for transform type allows movement within the 0 to 360 degree range, positive value = clockwise and negative = counterclockwise.

```css
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

- Through `scale`, we are able to change the size of an element. Default is `1` (100%); new syntax would have `scale(.75);`, or any other desired as the value.

- `translate` shifts / pushes and or pulls an element without having an impact on its surroundings, very similar to relative positioning. By the same logic, `translateX` and `translateY` change an elements position on the horizontal and vertical axis, respectively.  

As can be done with `scale` values, if you wish to set both at once in one rule rather than separately; the values must be separated with a comma within the parenthesis, with the value for `x` first, then `y`.  

```css
.box-3 {
  transform: translate(-10px, 25%);
}
```

- `skew` is used to distort elements on either or both axis. Syntax convention followed closely as to `scale` and `translate`. Distance is measured in units of degrees (`deg`); pixels and percentages not applicable.  

```css
.box-3 {
  transform: skew(5deg, -20deg);
}
```

### Combining Transforms

Common occurrence for multiple transforms to be applied to a single element; in this situation, only one `transform` property is used for all applicable transform types (`scale`, `skew`, etc.), syntax example shown below.  

```css
.box-2 {
  transform: skew(10deg, 20deg) translateX(20px);
}
```

### Transform Origin

The default transform origin position is the dead center of an element, halfway horizontally and vertically (50%).  
We are able to change this using `transform-origin` property and by using up to two values (x and y axis), but if only one is used then its applied to both axes.  

`0 0` is the same as `top left`; `100% 100%` is the same as `bottom right`.

```css
.box-1 {
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}
.box-2 {
  transform: scale(.5);
  transform-origin: 100% 100%;
}
```

Issues may arise when used in conjunction with `translate` since they are both attempting to position the element.

### 3D Transforms

Perspective is needed when working with three dimensional transforms. Set as a value for the `transform` property, `transform: perspective(10px)` on either the individual element or the parent element.  
The higher the `perspective` value, the further away its 'perceived' to be, and vice-versa.  
`perspective-origin` is also a value that can be modified.

- 3D `rotate` - adds `rotateZ`.
- 3D `scale` - `scaleZ`. Works best in conjunction with other 3D transforms
- 3D `translate` - `translateZ`

- 3D `skew` can't be transformed on a three dimensional aspect.

[Shorthand](https://developer.mozilla.org/en/CSS/transform-function) properties also exist; `rotate3d`, `scale3d`, `transition3d`, and `matrix3d`.

Nested elements that are being transformed suffer the consequence of inheritance if the parent element is being transformed itself. To allow the nested elements to transform, the `transform-style` property is used with the `preserve-3d` value on the elements desired.  
`transform-style: preserve-3d;`.

### Answers.1

1. What does a CSS transform allow the developer to do to an element?
    - change from one state to another; either `rotate`, `scale`, `translate`, `skew`.
2. Provide an example of a transform and how you could see that being used on a website.
    - change of color, shape, rotation; reaction to event. Buttons changing color, cursor pointer changing while hovering on an element.

## [CSS Transitions & Animations](http://learn.shayhowe.com/advanced-html-css/transitions-animations/)

Another update brought about with the rollout of CSS3. Transitions allow change between states, whereas animations set multiple points.  

### Transitions

Allows the alteration of appearance and behavior for an element whenever a state change happens. Different styles must be identified at each state, usually by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.  

Popular transition related properties include `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`.  
Example showing the two different states defined for a box changing `background` color;

```css
.box {
  background: #2db34a; // starting color
  transition-property: background; // property to change. may be mult; separated with comma
  transition-duration: 1s;  // time change takes to occur
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29; // new color
}
```

#### Properties

\* **Not all** properties may be transitional. Other common transitional properties include,  

- `background-color`
- `background-position`
- `border-color`
- `border-width`
- `border-spacing`
- `bottom`
- `clip`
- `color`
- `crop`
- `font-size`
- `font-weight`
- `height`
- `left`
- `letter-spacing`
- `line-height`
- `margin`
- `max-height`
- `max-width`
- `min-height`
- `min-width`
- `opacity`
- `outline-color`
- `outline-offset`
- `outline-width`
- `padding`
- `right`
- `text-indent`
- `text-shadow`
- `top`
- `vertical-align`
- `visibility`
- `width`
- `word-spacing`
- `z-index`

#### Duration

Set by the `transition-duration` property and values can be seconds (`s`), milliseconds (`ms`), and fractional seconds.  
If multiple properties are defined in `transition-property`, different durations may be used for each individual, matching up with the order, first property to first duration.

#### Timing

To set the speed at which the property will transition between stages; `transition-timing-function` is used.

- `linear` - moving from one state to another at a constant speed.
- `ease-in` - starts slow then finishes fast.
- `ease-out` - starts fast and finishes slow.
- `ease-in-out` - starts slow, speeds up, then finishes fast.

If transitioning multiple properties, same as duration; separate duration with comma.

#### Delay

Set with the use of `transition-delay` property and uses seconds or milliseconds.

A **[shorthand](https://learn.shayhowe.com/advanced-html-css/transitions-animations/#shorthand-transitions)** that can be used with all transitions is, `transition`.

### Animations

In order to specify the order the and changes of state for an animation, `@keyframes` is used where at minimum 2-3 different states are defined to animate. `@keyframes` is followed by the name of the animation, then inside the rule set we line out the 'breakpoints'/linear progression steps and the properties that will change at said breakpoint.

```css
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```

`@keyframes` is one of the new updates that **must** be prefixed.

- @-moz-keyframes
- @-o-keyframes
- @-webkit-keyframes

To apply created animations to elements, we use the `animation-name` property coupled with the name used after the `@keyframes` declaration, as a value.  
`animation-name: slide;`  

At minimum, an `animation-duration` property should also be declared so the browser knows how long to play the animation.  

`duration`, `timing-function`, and `delay` all also apply to animations.  
As well as the inclusion of `animation-iteration-count` to specify how many times one would like the animation to replay (number or `infinite`).  
`animation-direction` allows declaration of direction/flow (`normal`, `reverse`, `alternate`, and `alternate-reverse`).  
The ability to play or pause an animation is done through the use of the `animation-play-state` poperty and with `running` or `paused` values.  

### Answers.2

1. What does a CSS transition allow the developer to do to an element?
    - Allows changes to the element's property values over time, rather than instantly.
2. How does a CSS animation differ from a CSS transition?
    - Transition between two phases; animations over time, multiple steps.
    - animation is more controlled and more complex (implemented), can repeat forever; keyframes.

## [Simple, Grand CSS3 Transitions](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

`transition: all 0.3s ease;` will be the initial state. `all` properties will be affected, the speed for the change will be `.3` seconds, and `ease` as the default acceleration the change will occur.  

### Fade In

Used to emphasize functionality or draw attention to an object, action, etc. Required two steps to take effect; the initial/ default, then the changed state (what triggers it).

```css
.fade { // initial state; class applied to element
 opacity:0.5;
}

.fade:hover { // change on hover, 
 opacity:1;
}
```

### Change Color

```css
.color:hover { // 'hover' is the action that will bring the change from the initial state
 background:#53a7ea;
}
```

### Grow & Shrink

Old method involved having to specify dimensions, now we can use `transform: scale();`.

```css
.grow:hover { // action that bring about change
 -webkit-transform: scale(1.3); // vendor / browser compatability
 -ms-transform: scale(1.3); // ""
 transform: scale(1.3); // 
}
```

Inversely, shrinking is as simply. Growing involves a value greater than `1`, shrinking is less than `1`.

```css
.shrink:hover {
 -webkit-transform: scale(0.8);
 -ms-transform: scale(0.8);
 transform: scale(0.8);
}
```

### Rotate

```css
// pseudo class; hover
.rotate:hover {
 -webkit-transform: rotateZ(-30deg);
 -ms-transform: rotateZ(-30deg);
 transform: rotateZ(-30deg);
}
```

### Square to Circle

```css
.circle:hover {
 border-radius:50%;
}
```

### 3D Shadow

Done by adding a box shadow and using either `transform` or `translate` to move the element along the `x` axis. Work well to give users feedback on actions, events, or interaction.

```css
.threed:hover {
 box-shadow:
 1px 1px #53a7ea,
 2px 2px #53a7ea,
 3px 3px #53a7ea;
 -webkit-transform: translateX(-3px);
 transform: translateX(-3px);
}
```

### Swing

Done through the use of `@keyframes`, `animation`, and/or `animation-iteration`.

```css
@-webkit-keyframes swing {
 15% {
 -webkit-transform: translateX(5px);
 transform: translateX(5px);
 }
 30% {
 -webkit-transform: translateX(-5px);
 transform: translateX(-5px);
 } 
 50% {
 -webkit-transform: translateX(3px);
 transform: translateX(3px);
 }
 65% {
 -webkit-transform: translateX(-3px);
 transform: translateX(-3px);
 }
 80% {
 -webkit-transform: translateX(2px);
 transform: translateX(2px);
 }
 100% {
 -webkit-transform: translateX(0);
 transform: translateX(0);
 }
}
```

```css
@keyframes swing {
 15% {
 -webkit-transform: translateX(5px);
 transform: translateX(5px);
 }
 30% {
 -webkit-transform: translateX(-5px);
 transform: translateX(-5px);
 }
 50% {
 -webkit-transform: translateX(3px);
 transform: translateX(3px);
 }
 65% {
 -webkit-transform: translateX(-3px);
 transform: translateX(-3px);
 }
 80% {
 -webkit-transform: translateX(2px);
 transform: translateX(2px);
 }
 100% {
 -webkit-transform: translateX(0);
 transform: translateX(0);
 }
}
```

Use of both `@-webkit-keyframes` and `@keyframes` for compatibility sense.  

```css
.swing:hover {
 -webkit-animation: swing 1s ease;
 animation: swing 1s ease;
 -webkit-animation-iteration-count: 1;
 animation-iteration-count: 1;
}
```

### Inset

Can be used to style a 'ghost button'; a button that has a heavy border and no background in an easier manner then hard coding a border and box sizing.

```css
.border:hover {
 box-shadow: inset 0 0 0 25px #53a7ea;
}
```

### Answers.3

1. What are some benefits to using CSS transitions on websites?
    - Provides a natural feel to the user experience; gives visual feedabck to changes happening on screen in real time; emphasize certain pieces of content on a page; provide
2. How this topic fit in with your long-term goals?
    - This fits in by giving me more tools and expanding my knowledge to provide a better visual layout and elements in any HTML file I create.

## Psychological Safety

### [Lessons From Google](https://web.archive.org/web/20221125192300/https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

#### Answers.4

1. What are three key factors that contribute to psychologically safe teams?
    - Equal participation, respect and trust, comfort with exploring w/o risk of embarrassment.
2. Evaluate, with details, a previous professional setting (or team) you were in with regards to psychological safety.
    - shift passdowns when clocking in and clocking out at previous job.
3. What impact do teams that operate with a high degree of psychological safety have on their company and the team members?
    - better communication and better performance/efficiency/innovation.

## Bookmark/Skim

### [Pure CSS Bounce](http://codepen.io/dp_lewis/pen/gCfBv)

### [Buttons Animated](http://codepen.io/retyui/pen/ByoaXV)

### [CSS3 Animations: Keyframes](http://codepen.io/akshaychauhan/pen/oAfae)

### [404](http://codepen.io/kieranfivestars/pen/MYdQxX)

## Things I Want To Know More About

- transform, transition, and animation templates.
- best methods to combine diferent properties.
