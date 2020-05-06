# Positioning

## Relative:

Relatively positioned elements are offset a given amount from their normal position within the document

### Absolute:

An element that is absolutely positioned is taken out of the flow;

### Fixed:

Fixed positioning is similar to absolute positioning, with the exception that the element's containing block is the viewport.

## Sticky:

Sticky positioning can be thought of as a hybrid of relative and fixed positioning. A stickily positioned element is treated as relatively positioned until it crosses a specified threshold, at which point it is treated as fixed until it reaches the boundary of its parent.

## Normal Flow

Elements on a webpage lay out in the normal flow, if you have not applied any CSS to change the way they behave. And, as we began to discover, you can change how elements behave either by adjusting their position in that normal flow, or removing them from it altogether.

First of all, individual element boxes are laid out by taking the elements' content, then adding any padding, border and margin around them — it's that box model thing again, which we've looked at earlier.

By default, a block level element's content is 100% of the width of its parent element, and as tall as its content. Inline elements are as tall as their content, and as wide as their content. You can't set width or height on inline elements — they just sit inside the content of block level elements. If you want to control the size of an inline element in this manner, you need to set it to behave like a block level element with display: block; (or even,display: inline-block; which mixes characteristics from both.)
