+++
date = "2016-07-07T14:52:33-04:00"
next = "/week6/day28"
prev = "/week6/day26"
title = "Day 27: ECMAScript 6"
toc = true
weight = 3

+++

<date>Thursday, July 7, 2016</date>

## Topics

### [Exploring ES6](http://exploringjs.com/es6/index.html#toc_ch_first-steps)
A free eBook with tons of information about the new version of JavaScript.  A good place to start is [Chapter 4 - First steps with ECMAScript 6](http://exploringjs.com/es6/ch_first-steps.html)

### New features of ECMAScript 6 used in class
Block scoping - Great article [here](https://www.sitepoint.com/joys-block-scoping-es6/)

  * `let` for block-scoped variables without hoisting
  * `const` for immutable variables
  * Block-scoped functions - no need for IIFE's!

Arrow functions

```js
// Old way
numbers.map(function(x) { return x + 1; });

// ES6 way
numbers.map(x => { x + 1 })
```

Lexical scoping of `this` - article [here](https://toddmotto.com/es6-arrow-functions-syntaxes-and-lexical-scoping/)

```js
// Old way
this.nums.forEach(function(x) {
  if (x === 1)
    this.ary.push(x);
}.bind(this));

// ES6 way
this.nums.forEach(x => {
  if (x === 1)
    this.ary.push(x)
})
```

String interpolation

```js
// Old way
var message = "Hello, " + person.name + ",\n" +
"It is " + destination.distance + " miles to " + destination.place + "."

// ES6 way
let message = `Hello, ${person.name},
It is ${destination.distance} miles to ${destination.place}.`
```

Object property shorthand

```js
// Old way
obj = { x: x, y: y };

// ES6 way
obj = { x, y }
```

Classes

```js
class Example {
  constructor (a, b) {
    this.a = a
    this.b = b
  }
  otherFunction (x) {
    return x * 5
  }
}
```

## Projects
Meganote: [Morning](https://github.com/xternbootcamp16/meganote/tree/d254cc0b6903d42cc341cf36bb712f0f12b13bf1) | [Afternoon](https://github.com/xternbootcamp16/meganote/tree/ff163bfb68caf00240a345426be033e86b60da92)

Meganote-server: [Source](https://github.com/xternbootcamp16/meganote-server/tree/1bb67a3998459268681a21fb0f67c6572554a572)

## Homework

Modify your Meganote Server to allow it to create users

#### Base Requirement:  
Save users without passwords

#### Super Mega Bonus Credit:  
Verify that the password and password confirmation match before saving the user (still don't save the password, though)

#### Super Mega Bonus Credit Hyperfighting:
Store _encrypted_ passwords using `bcryptjs`
