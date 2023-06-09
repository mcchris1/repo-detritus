# React and Array Methods

## Goals

By the end of this exercise, you should have something that looks like the following:

![complete gif](./complete.gif)

## Setup

1. Fork,
1. Clone,
1. Install dependencies,
1. Get hacking!

## Part 1: Instructions

Inside of this repository, there's a React App with a few components. Your job is to use the array methods `filter`, `reduce`, `find`, and `some` to render some information about the flavors at **Ye Olde Ice Creame Shoppe**. The `.map()` has already been implemented in the `Map.jsx` component, as a demonstration. Each time you complete a component, check it in App.js. If you need a reference for any of these methods, use [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods).

### Filter

Open the `components` folder and open `Filter.jsx`. Within this component, filter over the `flavors` props for only flavors with chocolate chips. Take these filtered flavors and render a `Flavor` component for each one (use `Map.jsx`).

### Some

Open the `components` folder and open `Some.jsx`. Within this component, use the `some` method to find out if there are any flavors without chocolate chips. If there are flavors without chocolate chips, you should render the word "yes", otherwise render the word "no".

### Find

Open the `components` folder and open `Find.jsx`. Within this component, `find` a flavor with the word "Sorbet" in its `name`. Render the `name` of this flavor.

## Part 2: Instructions

Currently, the `.flavors` div has Flexbox implemented on it. While it is responsive, our flavors have gathered in the middle as opposed to being bound to the left side. Let's implement Grid in `App.css`!

### Changing Flex to Grid

On the `.flavors` div in `App.css`, remove the flex styling, and add the following:
1. Give the `.flavors` div a `display` property of `grid`.
2. Create 3 columns in this grid, of equal sizes (remember `fr`).
3. Create a gap between each item of 5px (remember `grid-gap`).

### Getting Responsive

The media query for our flavors div, unfortunately, also still uses flex.Let's change it to a single-column grid layout. On the media query for `.flavors`, add the following:

1. Create 1 column in this grid, using the `fr` measurement.
2. Change the gap between the items to 10px.

## Bonus

### Reduce

Open the `components` folder and open `Reduce.jsx`. Within this component, reduce the `flavors` array to a number—specifically the total number of flavors with chocolate chips. Take this number, and render how many flavors have chocolate chips.
