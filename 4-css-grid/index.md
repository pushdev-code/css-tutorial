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

## Let's practice

Please complete all the levels of [Grid Garden](https://cssgridgarden.com/)

<iframe src="https://cssgridgarden.com/" width="1024" height="768"></iframe>

## Exercise

1. From master `$ git checkout master`, create a new branch called `feature/css-grid-exercise`.
2. Create a new html file named `grid.html` with a css file named `styles.css` in `4-css-grid` folder.
3. Create this layout using CSS grid.
<img width="355" alt="Screen Shot 2020-05-09 at 11 56 06 AM" src="https://user-images.githubusercontent.com/668906/81480003-5d30a580-91ec-11ea-8a8f-7265514d31fa.png">

4. Push the changes to your local copy of the repo (Pull request).


## Source

* [CSS-Tricks-Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
