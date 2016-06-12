+++
date = "2016-06-11T17:09:05-04:00"
next = "/week1/day03"
prev = "/week1/day01"
title = "Day 2: Objects and Functions"
toc = true
weight = 2

+++

<date>Wednesday, June 1, 2016</date>

> [Solution to Tuesday's homework: FirstJS (Basic Form)](http://xternbootcamp16.github.io/firstjs-afternoon/)

## Topics

### Functions
* Function expressions
* Functions as variables
* Functions as object properties (_methods_)
* Variable scope
* IIFEs: Immediately Invoked Function Expressions
* Function invocation and the value of `this`
  * As functions, _e.g._ `someFunction()`: `this === window` (_i.e._ the global object)
    * **Warning**: This includes functions defined within other functions.
  * As methods, _e.g._ `someObject.someMethod()`: `this === someObject` (_i.e._ the object on which the method was called)
  * As event handlers, _e.g._ `someForm.onsubmit = someFunction`: `this === someForm` (_i.e._ the object that fired the event)

### Objects
* Object literals
* Property naming
* Retrieving property values
* Setting property values

### DOM
* Creating elements (`document.createElement('li')`)
* Setting style properties on elements (`someElement.style.backgroundColor = 'CadetBlue'`)
* Appending child elements (`someList.appendChild(someItem)`)

### Selectors
* Descendent (`ul li`) and child (`ul > li`)

### CSS Properties
* `background-color`
* `border`
* `height`
* `list-style`
* `width`

### Organizing Code
* `.js` files (`<script src="app.js"></script>`)
* Wrapping in an IIFE (`(function() {})();`)
* Wrapping in a object-literal (`{}`)

## Presentations
Presentations have been converted from their original format to play in web browsers.

* <a target="_blank" href="/presentations/week1/02-functions">Day 1 Review, Intro to Functions</a>

## Projects
* Finished Basic Form (FirstJS): [morning](https://github.com/xternbootcamp16/firstjs) | [afternoon](https://github.com/xternbootcamp16/firstjs-afternoon)

## Links

* [List of CSS color names](http://www.w3schools.com/colors/colors_names.asp)
* [IIFEs as explained by Ben Alman](http://benalman.com/news/2010/11/immediately-invoked-function-expression/), who coined the term
* [More than you ever wanted to know about _objects_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

## Homework: Megaroster

Create a class roster.

### Baseline Goal
* User can enter a name to be added to the roster.
* Name will be added to the end of a list

### Bonus Credit
* Create _at most_ one global variable.

### Mega Bonus Credit
* Add names to the _top_ of the list.

### Super Mega Bonus Credit
* Add a _delete_ link to every list item that removes the name from the list when clicked.

### Super Mega Bonus Credit Hyper Fighting
* Add a _promote_ link to every list item that draws a border around that item when clicked.

> **Update**: [Solution: MegaRoster with delete and promote](https://github.com/xternbootcamp16/megaroster-afternoon/tree/dfa5fbf687e0eb39fe6e60837eda35778c7e860a)
