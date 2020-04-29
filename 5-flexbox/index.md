# Flexbox

* Flexbox is a one-dimensional layout method for laying out items in rows or columns. 
* Items flex to fill additional space and shrink to fit into smaller spaces.

Visit [Visual CSS Flexbox](http://www.csstutorial.org/flex-both.html)

* The main idea behind the flex layout is to give the container the ability to alter its items' width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). 
* A flex container expands items to fill available free space or shrinks them to prevent overflow.

Image of Flexbox axis

![Box Model](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg)

* Most importantly, the flexbox layout is direction-agnostic as opposed to the regular layouts (block which is vertically-based and inline which is horizontally-based). 
* While those work well for pages, they lack flexibility (no pun intended) to support large or complex applications (especially when it comes to orientation changing, resizing, stretching, shrinking, etc.).
* Since flexbox is a whole module and not a single property, it involves a lot of things including its whole set of properties. 
* Some of them are meant to be set on the container (parent element, known as "flex container") whereas the others are meant to be set on the children (said "flex items").

![image](https://user-images.githubusercontent.com/61557537/80294555-a0d8d900-872f-11ea-9e94-fcf3c360a65e.png)

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
## Let's practice


Please complete all the levels of [Flexbox Froggy](https://flexboxfroggy.com/)

<iframe src="https://flexboxfroggy.com/" width="1024" height="768"></iframe>

## Exercise

1. Use the `index.html` int the `assets` folder inside `5-flexbox` folder.
2. Create the `styles.css` file.
3. Build a layout using flexbox.
4. Play with the different properties.
5. Now you can use flexbox in your html-form.


* Create a new branch called /feature/css-flexbox-yourname
* Push the changes to your local copy of the repo (Pull request).


## Source

* [CSS-Tricks-Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [Flexbox tutorial](https://medium.com/@js_tut/the-complete-css-flex-box-tutorial-d17971950bdc)
