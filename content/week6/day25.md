+++
date = "2016-07-05T15:37:48-04:00"
next = "/week6/day26"
prev = "/week6"
title = "Day 25: Review"
toc = true
weight = 1

+++

<date>Tuesday, July 5, 2016</date>

## Topics

### JavaScript
  * Hoisting - Function and variable declarations are always hoisted to the top of their containing scope by the JavaScript interpreter.  Variable assignments are not hoisted.
  * [Function Declarations vs Function Expressions](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/) - A quick overview of hoisting with examples
  * [Scoping and Hoisting](http://www.adequatelygood.com/JavaScript-Scoping-and-Hoisting.html) - A more in-depth look at scoping and hoisting

So this:

```js
function foo() {
  bar();
  var x = 1;
}
```

Is interpreted as:

```js
function foo() {
  var x;
  bar();
  x = 1;
}
```

### AngularJS
  * `controllerAs`
  * `resolve`
  * Factories
  * Custom Directives
    * Default use is as attribute or element (as of Angular 1.3)
    * `bindToController` - binds isolate scope properties to controller for use with `controllerAs` syntax
  * Style
    * Function declarations over function expressions
    * `activate()` functions for resolving start-up logic for a controller
    * Bindable / Accessible members up top

## Homework
Continue working on refactor of Meganote.  If you need to start from a fresh copy, the repo in its current state can be cloned [here](https://github.com/xternbootcamp16/meganote/commit/2fcc8902aefb6a202adefb55f3d70bdc445166f1)
