# CSS

Cascading Style Sheets

## The basics

CSS allows to change the look & feel of the HTML.

```html
  <body>
  <h1>First example with CSS</h1>
  <header>
    <p>Welcome to the first CSS example</p>
  </header>
  <main>
    <article>
      <p>
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's
        standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make
        a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting,
        remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing
        Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions
        of Lorem Ipsum.
      </p>
      <ul>
        <li>item 1</li>
        <li class="selected-item">item 2</li>
        <li>item 3</li>
        <li>item 4</li>
      </ul>
    </article>
  </main>
  <footer>
    <a href="https://pushdev.co">Visit our webpage</a>
    <p>© PushDev 2020</p>
  </footer>
</body>
```

### Syntax

Rule-based language: The color of the `<h1>` should be white and its font size should be 14px.

```css
h1 {
  color: white;
  font-size: 14px;
}
```

![image](https://user-images.githubusercontent.com/61557537/80286303-36ed0f00-86f0-11ea-8e3c-4e1e5be4f425.png)

A stylesheet may contain several rules, but be careful how you organize your code.

```css
h1 {
  color: white;
  font-size: 14px;
}

p {
  color: white;
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

### Change the background

* `color` is referring to the text color in that element.
* `background-color` refers to the background color.
* `background` is shorthand to combine many background tags into one line.

```css
body {
    background-image: url('./bg.jpeg');
    background-size: cover;
}

li:hover {
    background-color: rgba(255, 255, 255, 0.7); 
}

main {
    background: rgb(0, 28, 153) no-repeat right top;
}
```

### CSS Specificity

Style attribute ----> ID ----> Class, pseudo-class attribute ----> Elements

Image of Specificity

![CSS Specificity](https://css-tricks.com/wp-content/csstricks-uploads/cssspecificity-calc-1.png)

### Selectors Task

Please complete all levels on https://flukeout.github.io/

### Exercise

We are going to apply styles to the HTML form that we created in the [HTML Tutorial](https://pushdev-code.github.io/html-tutorial/)

1. Change the color of the `<header>` and the `<footer>`.
2. Set a `background-image` to the element that contains the `<form>`.
3. Change the `background-color` of the `<form>`.
4. Apply the `:hover` pseudo-class to the buttons.
5. Change the `font-size`, `font-weight`, `font-family` and the `color` of the text in the elements that you want.
6. Set a `background` to the `<footer>`.

* Create a new branch called `/feature/css-basic-yourname`
* Push the changes to your local copy of the repo (Pull request).

## Source

* [Introduction to CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Introduction)
