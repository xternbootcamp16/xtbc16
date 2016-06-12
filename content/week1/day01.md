+++
date = "2016-06-11T16:29:51-04:00"
next = "/week1/day02"
prev = "/week1"
title = "Day 1: Introduction"
toc = true
weight = 1

+++

<date>Tuesday, May 31, 2016</date>

## Topics
* History of JavaScript and the Web
* Getting the most out of a coding bootcamp
* Anatomy of an HTML element (tags, attributes, contents)
* Basic CSS selector syntax
  * Element name (`div`, `h1`, `p`, etc.)
  * Element ID (`#theID`, `div#theID`, etc.)
  * Class name (`.theClass`, `p.theClass`, etc.)
* Basic DOM manipulation
  * `document.querySelector`/`document.querySelectorAll`
  * `.innerText`/`.innerHTML`
* Basic event handling
  * `onsubmit`
  * Anonymous functions
  * `.preventDefault`

## Presentations
Presentations have been converted from their original format to play in web browsers.

* <a target="_blank" href="/presentations/week1/01-javascript-history">JavaScript History</a>
* <a target="_blank" href="/presentations/week1/js-bootcamp-expectations-tips">Bootcamp Expectations and Tips for Success</a>

## Projects
* Basic Form (FirstJS):  [morning](https://github.com/xternbootcamp16/firstjs) | [afternoon](https://github.com/xternbootcamp16/firstjs-afternoon)

## Links

* [Foundation](http://foundation.zurb.com/) - a front-end framework
* [CSS Diner](http://flukeout.github.io/) - a game for practicing CSS selector syntax
* [CSS Selector Game](http://toolness.github.io/css-selector-game/) - another tool for practicing selector syntax

## Homework: Basic Form (FirstJS)

Grab values from form fields and add them to a list.

You'll need to employ these concepts that we used in class:
* Target elements with `document.querySelector`
* Handle events
* Prevent default event behavior from executing
* Alter an element's contents via `innerHTML`

### Baseline Goal
* Display values as plain text.

### Bonus Credit
* Display values in separate paragraphs.

### Mega Bonus Credit
* Display values in an unordered list.

### Super Mega Bonus Credit
* Display values in a _definition list_ (`<dl>`).

Output something like this:

```html
<dl>
  <li>
    <dt>First Name</dt>
    <dd>Davey</dd>
  </li>

  <li>
    <dt>Hair color</dt>
    <dd>#000000</dd>
  </li>

  <!-- etc. -->
</dl>
```

### Super Mega Bonus Credit Hyper Fighting

Display the color value _in the specified color_.

> **Update**: [Solution: FirstJS (Basic Form)](http://xternbootcamp16.github.io/firstjs-afternoon/)
