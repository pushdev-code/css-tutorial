# CSS Grid

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
