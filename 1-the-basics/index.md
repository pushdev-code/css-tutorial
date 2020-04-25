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
