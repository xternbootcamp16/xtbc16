+++
date = "2016-06-17T13:16:56-04:00"
next = "/week3/day14"
prev = "/week3/day13"
title = "Day 14: Wrapping up Meganote"
toc = true
weight = 5

+++

<date>Friday, June 17, 2016</date>

## Topics

### Markdown
  * [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) - An overview of Markdown from Github
  * [Markdown Tutorial](http://www.markdowntutorial.com/) - a quick, interactive tutorial for the basics

  {{% notice tip %}}
  Add a `README.md` Markdown file to your projects to explain setup and usage.  Your users and your future self will thank you.
  {{% /notice %}}

### CORS
  * [CORS W3C specification](https://www.w3.org/TR/cors/)
  * `Access-Control` headers to specify what types of requests and methods are allowed
  * [Cross-Origin Requests in Express.JS](http://justindavis.co/2015/08/31/CORS-in-Express/)

### Mongoose
  * `.sort()`
  * `.findOne()`
  * [Middleware / Hooks](http://mongoosejs.com/docs/middleware.html)
    * Set up events to occur before or after a supported Document, Query, or Model function
    * `schema.pre('save')` - to occur before a `save` function
    * `schema.post('save')` - to occur after a `save` function

### Third-Party Packages added to Meganote
  * [Sanitize HTML](https://www.npmjs.com/package/sanitize-html) (Node)
  <br>Clean up user-submitted HTML, preserving whitelisted elements and whitelisted attributes on a per-element basis.
  * [HTML-to-Text](https://www.npmjs.com/package/html-to-text) (Node)
  <br>An advanced converter that parses HTML and returns beautiful text.
  * [textAngular](http://textangular.com/) (Angular)
  <br>A Lightweight, Two-Way-Bound & Totally Awesome Angular.js Text-Editor.

### More `ui-router`
  * [`ui-sref`](http://angular-ui.github.io/ui-router/1.0.0-alpha.3/modules/ng1_directives.html#uisrefng1) - A directive that binds an anchor tag (`<a>`) to a state
  * [URL Routing with Parameters](https://github.com/angular-ui/ui-router/wiki/URL-Routing#url-parameters)
  * [Nested States and Views](https://github.com/angular-ui/ui-router/wiki/Nested-States-%26-Nested-Views) - Also known as child states
  * [Resolve](https://github.com/angular-ui/ui-router/wiki#resolve) - Provides your controller with content or data that is custom to the state.  Any promises will be resolved and converted to a value _before_ instantiating the controller.

### More Angular
  * `ng-bind-html` - tells Angular to replace the innerHTML of an element with the value of an expression.  Similar to `{{ expression }}`
  * `.constant` - register a Provider on an angular module that returns a constant value

  ```js
  angular.module('myApp')
    .constant('API_URL', 'http://myapi.com/example/all');
  ```
