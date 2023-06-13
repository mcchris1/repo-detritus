[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# CSS Grid

So far, we've talked about the box model and flexbox to adjust the alignment of items on our web pages. Next, we'll cover **CSS Grid** for laying out the key components of a webpage. 

## Objectives

By the end of this, developers should be able to:

- Explain what CSS Grid is and what problem it solves
- Use CSS Grid to create a page layout.
- Explain when to use Flexbox versus CSS Grid

## What is CSS-Grid Layout?

From the [www.w3.org](https://www.w3.org/TR/css-grid-1/) website:

> "Grid Layout is a new layout model for CSS that has powerful abilities to
> control the sizing and positioning of boxes and their contents. Unlike
> Flexible Box Layout, which is single-axis–oriented, Grid Layout is optimized
> for 2-dimensional layouts: those in which alignment of content is desired in
> both dimensions."

With Grid layout, you can divide up the screen into `rows` and `columns` of
sizes of your choosing, and then specify how many rows and columns each `cell`
takes up. Sizing can be fixed, or dynamic, allowing you to create modern
looking, versatile websites.

_Example of elements arranged with **flexbox**_

![flex layout example](assets/flex-layout-ex.png)

_Example of elements arranged with **grid**_

![grid layout example](assets/grid-layout-ex.png)

Notice that the grid items are aligned (rather than filling up the available space) and that cells can take up multiple rows or columns.

## I Do: Explore the Source Code

1. To start, you must have a _container_ (or _parent_) element, with at least
   one _nested_ (or _child_) element inside.

```html
<div class="parent">
  <div class="child child-one">1</div>
  <div class="child child-two">2</div>
  <div class="child child-three">3</div>
</div>
```

2. On the container, specify that you are using `display: grid` and what the size and structure of your
   **_template_** will look like - more specifically, your **_rows_** and
   **_columns_**. Here's an example.

```css
.parent {
  display: grid;
  grid-template-rows: 100px 200px 300px;
  grid-template-columns: 100px 1fr 2fr 100px;
}
```

`px` represents pixels - a unit that you have seen before in CSS with property values like 
`font-size`, `margin` and `padding`! You would use pixels if you have an exact size in mind for 
each or your rows and columns.

The `fr` unit stands for _fraction_ and is used to evenly span the remainder of the space. 

> `grid-template` also takes other units like `%`, `rem`, and `auto`.
> For now we will focus on `px` and `fr` units. You can also use `repeat` to
> specify multiple rows or columns of one size like this `repeat(5, 1fr)`

Here, we have specified **_3 rows_**, taking up 100, 200, and 300 pixels
respectively. We also specified **_4 columns_**, giving us a total of **_12
cells_**. 

3. the _child_ elements, you can specify where the _cells_ are located and the
   _size you want them to be. I like to follow this pattern:

```css
selector {
  grid-row: where-to-start / span-size;
}
```

- `where-to-start` indicates the row in which you want the child element to begin. In this 
example, we have three rows to choose from: 1 is 100px, 2 is 200px and 3 is 300px
- `span-size` indicates how many rows you want the element to take up. In this example, a 
span of 1 would be equal to 100px, but a span of 2 would be equal to 200px (rows 1 and 2 added
together)

> It works the same way for the `grid-column` property

So a _child_ element will look something like this:

```css
.child-one {
  grid-row: 1 / span 1;
  grid-column: 1 / span 2;
}
```

This element takes up 1 row, starting at row 1, and takes up 2 columns, starting
at column 1.

We could also write `grid-row: 1;` for short, if your element only spans 1 row.

## The Holy Grail Layout (5 min / 1:20)

![holy grail layout](assets/holy-grail-layout.png)

The holy grail layout is something you know well, even if you don't recognize the term. It
describes a webpage with a header, footer, and three columns: a wide "main"
column, a navigation column on the left, and an advertisement, site map, or
extra info column along the right.

Obviously, this layout won't work on tiny screens, unless you really like
super-skinny columns. It's common to stack things on top of each other for
mobile views to make one single column.

Before flexbox, this involved a lot of pushing and shoving with dimensions and
positioning. You would essentially have to write two completely separate
stylesheets (one for mobile, and one for desktop), each to control the different
layouts.

You can also create the holy grail layout on your web page with CSS grid!

## I Do: Griddle Me This

[Follow along here](https://codepen.io/perryf/pen/rJNZpw)

Let's follow along and try to make our _holy grail_ website design using
Grid layout. We will need a header, a footer, two side columns, and a main
section.

First, we will add our `grid-template` code to our parent element.

```css
body {
  display: grid;
  grid-template-rows: 80px 1fr 80px;
  grid-template-columns: 100px 1fr 100px;
}
```

Now let's figure out how to format our `header`. We want the header to take up 1
row and 3 columns. Let's give it some color too.

```css
header {
  grid-row: 1;
  grid-column: 1 / span 3;
  background: steelblue;
}
```

Now onto our left column. That will only take up 1 column and one row, starting
at row 2.

```css
.left {
  grid-row: 2;
  grid-column: 1;
  background: lightseagreen;
}
```

The right column can be positioned in a very similar fashion.

```css
.right {
  grid-row: 2;
  grid-column: 3;
  background: mistyrose;
}
```

The main section is the largest section (except on tiny screens) but really only
takes up one row and one column.

```css
main {
  grid-row: 2;
  grid-column: 2;
  background: lemonchiffon;
}
```

Lastly, our footer will take up the entire bottom row, spanning 3 columns.

```css
footer {
  grid-row: 3;
  grid-column: 1 / span 3;
  background: rebeccapurple;
}
```

**[Solution on Codepen](https://codepen.io/perryf/pen/eVYbGv)**

## Closing

Flexbox and Grid compliment each other well by design. 
In general, grids are best for a website's overall layout and flexbox is best for distributing components within the layout. 


## Review Questions

- Why is alignment so important with modern web development?
- What problems do Flexbox and Grid solve?
- Where do I put `display: flex` or `display: grid`?
- With flexbox, what are some properties that `justify-content` can take?
- Explain how to place an item into a grid container.

## Additional Resources

- [CSS Grid Garden](http://cssgridgarden.com/)
- [The CSS `grid` Module](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Learn CSS Grid](http://learncssgrid.com/)

## [License](LICENSE)

1. All content is licensed under a CC­BY­NC­SA 4.0 license.
1. All software code is licensed under GNU GPLv3. For commercial use or
   alternative licensing, please contact legal@ga.co.
