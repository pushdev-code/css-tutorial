# CSS

Cascading Style Sheets

## The basics

CSS allows to change the look & feel of the HTML.

### Syntax

Rule-based language: The color of the main heading should be blue and its font size should be 14px.

```css
h1 {
  color: blue;
  font-size: 14px;
}
```

A stylesheet may contain several rules, but be careful how you organize your code.

```css
h1 {
  color: blue;
  font-size: 14px;
}

p {
  color: red;
  font-style: italic;
}
```

### How to add CSS to our HTML

Inline using the style attribute for each HTML element:

```html
<p style="color: blue; font-size:18px;">This paragraph should be blue and with 18px of size</p>
```
Using the style tag in the <head> section of the page:

```html
<style>
h1 {
  color:red;
}
p {
  color:blue;
}
</style>
```

Referencing a CSS file:

```html
<link rel="stylesheet" href="styles.css">
```

### Changing the default browser styles

```css
li {
  list-style-type: none;
}

a {
  text-decoration: none;
}

p {
  margin: 0;
}
```

### Using the class attribute in the elements.

```html
<ul>
  <li>item 1</li>
  <li class="selected-item">item 2</li>
  <li>item 3</li>
  <li>item 4</li>
</ul>
```
CSS code:

```css
.selected-item {
  color: blue;  
}
```

More specific:

```css
li.selected-item {
  color: blue;  
}
```

Group of selectors can be specified in the same block:

```css
li.selected-item,
span.selected-item {
  color: blue;  
}
```

### Using the ID attribute in the elements.

```html
<ul>
  <li>item 1</li>
  <li id="selected-item">item 2</li>
  <li>item 3</li>
  <li>item 4</li>
</ul>
```
CSS code:

```css
#selected-item {
  color: blue;  
}
```

### Styling based on the location of the elements.

```html
<article>
  <h1>This is a title</h1>
  <p>Current time is: <time>17:40</time></p>
</article>
```

```css
article p time {
  color: red;  
}
```

When it comes to next other elements:

```css
h1 + p {
    font-size: 200%;
}
```

### Styling elements based on state

```html
<p>This is a <a href="https://google.com">link</a></p>
```

```css
a:hover {
  color: green;
}

a:visited {
  color: pink;
}
```

### CSS Specificity

Style attribute ----> ID ----> Class, pseudo-class attribute ----> Elements

Image of Specificity

![CSS Specificity](https://css-tricks.com/wp-content/csstricks-uploads/cssspecificity-calc-1.png)

### Selectors Task

Please complete all levels on https://flukeout.github.io/

## Layouts

CSS Page layout techniques allows web developers to control the position of the elements in a web page.

    * Box Model
    * Positioning
    * Normal flow
    * Display property
    * Flexbox
    * CSS Grid
    * Floats

### Box Model

CSS box model is a container which contains multiple properties including borders, margin, padding and the content itself. It is used to create the design and layout of web pages. It can be used as a toolkit for customizing the layout of different elements. The web browser renders every element as a rectangular box according to the CSS box model.
Box-Model has multiple properties in CSS. Some of them are given below:

* borders
* margins
* padding
* Content

Image of Box Model

![Box Model](https://www.csssolid.com/images/CSSBoxModel.png)

### Positioning

### Relative:

Relatively positioned elements are offset a given amount from their normal position within the document

#### Absolute:

An element that is absolutely positioned is taken out of the flow;

#### Fixed:

Fixed positioning is similar to absolute positioning, with the exception that the element's containing block is the viewport.

#### Sticky:

Sticky positioning can be thought of as a hybrid of relative and fixed positioning. A stickily positioned element is treated as relatively positioned until it crosses a specified threshold, at which point it is treated as fixed until it reaches the boundary of its parent.

## Normal Flow

Elements on a webpage lay out in the normal flow, if you have not applied any CSS to change the way they behave. And, as we began to discover, you can change how elements behave either by adjusting their position in that normal flow, or removing them from it altogether.

First of all, individual element boxes are laid out by taking the elements' content, then adding any padding, border and margin around them — it's that box model thing again, which we've looked at earlier.

By default, a block level element's content is 100% of the width of its parent element, and as tall as its content. Inline elements are as tall as their content, and as wide as their content. You can't set width or height on inline elements — they just sit inside the content of block level elements. If you want to control the size of an inline element in this manner, you need to set it to behave like a block level element with display: block; (or even,display: inline-block; which mixes characteristics from both.)

## Flexbox

Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces.

The main idea behind the flex layout is to give the container the ability to alter its items' width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). A flex container expands items to fill available free space or shrinks them to prevent overflow.

Image of Flexbox axis

![Box Model](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg)

Most importantly, the flexbox layout is direction-agnostic as opposed to the regular layouts (block which is vertically-based and inline which is horizontally-based). While those work well for pages, they lack flexibility (no pun intended) to support large or complex applications (especially when it comes to orientation changing, resizing, stretching, shrinking, etc.).

Since flexbox is a whole module and not a single property, it involves a lot of things including its whole set of properties. Some of them are meant to be set on the container (parent element, known as "flex container") whereas the others are meant to be set on the children (said "flex items").

If "regular" layout is based on both block and inline flow directions, the flex layout is based on "flex-flow directions". Please have a look at this figure from the specification, explaining the main idea behind the flex layout.

```css
.flex-container {
  /* We first create a flex layout context */
  display: flex;

  /* Then we define the flow direction
     and if we allow the items to wrap
   * Remember this is the same as:
   * flex-direction: row;
   * flex-wrap: wrap;
   */
  flex-flow: row wrap;

  /* Then we define how is distributed the remaining space */
  justify-content: space-around;
}
```

## CSS Grid

CSS Grid Layout is a two-dimensional layout system for the web. It lets you lay content out in rows and columns, and has many features that make building complex layouts straightforward.

Image of Grid columns and rows

![Grid system](https://mdn.mozillademos.org/files/13899/grid.png)

A grid is a collection of horizontal and vertical lines creating a pattern against which we can line up our design elements. They help us to create designs where elements don’t jump around or change width as we move from page to page, providing greater consistency on our websites.

A grid will typically have columns, rows, and then gaps between each row and column — commonly referred to as gutters.

```css
.grid-container {
  display: grid;
  grid-template-columns: 250px 250px 250px 250px 250px;
  grid-template-rows: 150px;
  grid-gap: 30px;
}
```

## Media queries

The CSS Media Query gives you a way to apply CSS only when the browser and device environment matches a rule that you specify, for example "viewport is wider than 480 pixels". Media queries are a key part of responsive web design, as they allow you to create different layouts depending on the size of the viewport, but they can also be used to detect other things about the environment your site is running on, for example whether the user is using a touchscreen rather than a mouse.

### Syntax:

```css
@media media-type and (media-feature-rule) {
  /* CSS rules go here */
}
```

* Media type, which tells the browser what kind of media this code is for (e.g. print, or screen).
* The media expression, which is a rule, or test that must be passed for the contained CSS to be applied.
* The set of CSS rules that will be applied if the test passes and the media type is correct.


## Final CSS Test

Chose one layout to build it. It should behave as showed in the animated gif.

Layout 1: https://cdn-images-1.medium.com/max/1600/1*aN_Im5EoU8hswHF2Hkpksw.gif

![Layout 1](https://cdn-images-1.medium.com/max/1600/1*aN_Im5EoU8hswHF2Hkpksw.gif)

Layout 2: https://cdn-images-1.medium.com/max/1600/1*7JLljCGtZXZySxVPbns1Og.gif

![Layout 2](https://cdn-images-1.medium.com/max/1600/1*7JLljCGtZXZySxVPbns1Og.gif)


Layout 3: https://cdn-images-1.medium.com/max/1600/1*P9QGSeySIUM14lsFDYL-rw.gif

![Layout 3](https://cdn-images-1.medium.com/max/1600/1*P9QGSeySIUM14lsFDYL-rw.gif)


Layout 4: https://cdn-images-1.medium.com/max/1600/1*1H1YXZtgYpRjJY8Xp05LpQ.gif

![Layout 4](https://cdn-images-1.medium.com/max/1600/1*1H1YXZtgYpRjJY8Xp05LpQ.gif)
