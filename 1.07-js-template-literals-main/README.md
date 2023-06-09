<img src="https://i.imgur.com/ZVquCx6.png" width="100%">

# ES2015 Template Literals Walk-Through

## Road Map

1. What are Template Literals?
2. Features of Template Literals

## 1. What are Template Literals?

**Template literals** are a third way to **define** and **use** strings in JavaScript.

Template literals were added to JS with the ES2015 specification.

Of course, you're already familiar with using single-quotes to delimit strings:

```js
let myString = 'This is my string';
```

...and double-quotes:
 
```js
let myString = "This is my string";
```

Now we can use the back-tick (below the `[esc]` key) too:

```js
let myString = `This is my string`;
```

Why a third option?  Read on...

## 2. Features of Template Literals

Let's look at the features template literals provide...

### String Interpolation

One of the most enjoyable things we do as developers is concatenating string after string after string... Not!

```js
const person = {
  firstName: 'Albert',
  lastName: 'Einstein',
  born: 1879,
  note: 'genius'
};

let result = person.firstName + ' ' + person.lastName + ' was born in ' +
	person.born + ' and was a ' + person.note + '.';
	
// Albert Einstein was born in 1879 and was a genius.
```

Using template literals, we can "embed" JS expressions within a string using interpolation:

```js
let result = `${person.firstName} ${person.lastName} was born in ${person.born} and was a ${person.note}.`;
	
// Albert Einstein was born in 1879 and was a genius.
```

Any JS expression, including function calls, can be inserted between the `${` and `}` characters.

### Multi-Line Strings

In non-template literals, we could create line breaks using the newline character - `\n`:

```js
let twoLines = 'This is line one.\nThis is line two.';
```

However, you will get a syntax error if you try this:

```js
let twoLines = 'This is line one.
This is line two.';
```

But not with template literals!

```js
let twoLines = `This is line one.
This is line two.`;
```

In fact, all white space (spaces, tabs & new lines) is honored within template literals. This can be convenient when the time comes to define HTML within a string:

```js
let htmlTemplate =
  `
  <div class="panel">
    <div class="title">${person.firstName} ${person.lastName}</div>
    <div class="content">
      <p>Born: ${person.born}</p>
      <p>Note: ${person.note}</p>
    </div>
  </div>
  `;
```

### Tagged Template Literals

Tagging template literals is an advanced use case of template literals.

A tagged template literal is a template literal prefaced with a function.

The string is "processed" by the function and whatever the function returns will be considered the actual value of the string:

```js
const person = "Chris";
const age = 100;

function myTag(strings, personExp, ageExp) {
    const str0 = strings[0]; // "That "
    const str1 = strings[1]; // " is one of those "
    const str2 = strings[2]; // "s."

    const ageStr = ageExp > 99 ? "oldster" : "youngster";

    // We can build a new string using a template literal
    return `${str0}${personExp}${str1}${ageStr}${str2}`;
}

const output = myTag`That ${person} is one of those ${age}s.`;

console.log(output);
// That Chris is one of those oldsters.
```

The first argument is an array of template strings. The string passed to the
function is split up into this array of stringcs using the expression as the
separator.

```js
`This string ${expression1} would be split ${expression2} like this.`

// [`This string`, `would be split`, `like this`]
``` 

The evaluated expressions are the subsequent arguments to the function.

```js
`If I used this string, ${expression1} the arguments ${expression2} for a tagged
template literal ${expression3} would have parameters that look like this.

// someTagFunction(strings, expression1, expression2, expression3) {
    ... some function behavior
}
```


This provides lots of flexibility when transforming the string **BUT**, their
use is not common. It's not super important to understand this 100%  but feel
free to check them out in [MDN's docs for Template
Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
and/or check out [this article](https://www.tektutorialshub.com/javascript/tagged-templates-in-javascript/)
if you're interested in learning more!
