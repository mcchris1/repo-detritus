[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Fetch & Promises

## Objectives

By the end of this, developers should be able to:

- Perform GET requests to an API to retrieve data
- Render new HTML content using data loaded from an AJAX request

## Promises & Asynchronous JS

An AJAX request is asynchronous: we'll make our request to the server and some
time later will get our response. In the meantime, the rest of our code will
keep running. We need some way to handle it when it's finished. We've previously
handled asynchronous actions by using callbacks. The `.fetch()` method uses
**Promises**.

Asynchronous also means that things won't run in the order that you expect them
to. Here's an example:

```js
const url = 'https://swapi.dev/api/people'

console.log(1);

fetch(url)
    .then(res => {
        if (res.ok) {
            console.log(`ok`, 2);
            console.log(res);
        }
    })
    .catch(err => console.log('oops something went wrong', err));

console.log(3);
```

> Try it! You might be surprised that you'll see 1, 3, 2 in the console.

You'll notice there are 2 functions _chained_ onto the AJAX call. These are our
**promise methods**. Promises are callbacks that may or may not happen. A
promise represents the _future result_ of an asynchronous operation. It's how we
handle the return value of our `fetch` request.

- `.then()` - this code is run if the Promise is fulfilled
- `.catch()` - this code is run if the Promise is rejected
- `.finally()` - this code is always run, fulfilled or not

Note that .then() will be called even if we get a 404 or some other error code
from our requested URL. This is because the response back is still considered a
fulfilled promise. The response will however include a property `ok: false`
which you can use to control the flow of your code.

Ex:

```js
const url = 'https://swapi.dev/api/dog'

fetch(url).then(res => {
    if (res.ok) {
        console.log("celebrate!");
    } else {
        console.log(`not ok`, 2)
        console.log(res);
    }
});
```

## The API Response

When we were working with the Star Wars API before, we saw a JSON object in the
browser that consisted of data about different People, Planets and
Spaceships of the Star Wars universe. How do we access this JSON object? If we use `.then()` we can
log out information about the response on the page. However, we can't do much
with the body of the data yet. Luckily, our response has a `.json()` method that
can be called which will turn our response into JSON.

Let's update the `script.js` file to incorporate this.

```js
const url = 'https://swapi.dev/api/people/1'
fetch(url)
    .then(res => {
        return res.json();
    })
    .then(res => {
        console.log("success!", res);
    })
    .catch(err => {
        console.log("something went wrong...", err);
    });
```

What we have above is an example of **chaining**. You are almost guaranteed to
have to work with chaining when dealing with AJAX or Promises. I like to
short-hand the above code to something like this...

```js
fetch(url)
  .then(res => res.json())
  .then(res => console.log("success!", res))
  .catch(err => console.log("something went wrong...", err));
```

We can then dig through this response just like any other JS object to pull up
the information we want.

```js
.then(res => console.log(res.name))
```

## I Do: DOM Manipulation Using Response Data

1. Let's add a form and a `<h1>` to the HTML. The form should include a single text input and a submit button.
1. We'll add an event listener to our form so that when submitted, we trigger an AJAX call to the Star Wars API to find the `Person` with the value from the text input field in the form.
   - So if you type `1` in the input, it will return `Luke Skywalker`.
2. Inside the `.then()` promise callback, handle the response and set the text of your `<h1>` to be the `Luke's` full name.

> Hint: What does `.preventDefault()` do?

## You Do: More Requests / DOM Manipulation Practice

Using the API docs as reference, let's explore outputting a list of items.

We can use the base URL of any of the resources, like `/starships` or `/planets` to get a list of those things. The API only returns various amounts of responses depending on how which endpoint you hit.

Use that info plus our knowledge of DOM methods to make a list of `starship` names.

- Get the list of `starships` from the API
- Loop through the list of `starships`, making an HTML element from each
- Append the HTML element to the DOM in an `li` tag

## You Do: Add URLs to Each Element

Using the previous logic, what would we need to change to add the `url` property from the `starships` results to the DOM?


## Additional Resources

- [API Keys](/apiKeysExercise.md)
- [Fetch, jQuery, XMLHttpRequest](/fetch-jquery-xml.md)
- [jQuery AJAX Cheat Sheet](/jQuery-ajax-cheatsheet.md)

## [License](LICENSE)

1. All content is licensed under a CC­BY­NC­SA 4.0 license.
1. All software code is licensed under GNU GPLv3. For commercial use or
   alternative licensing, please contact legal@ga.co.
