+++
date = "2016-06-13T16:19:37-04:00"
next = "/week3/day10"
prev = "/week3"
title = "Day 10: ui-router Basics"
toc = true
weight = 1

+++

<date>Monday, June 13, 2016</date>

## Topics

### `ui-router`
* [Getting Started with `ui-router`](https://github.com/angular-ui/ui-router#get-started)
* [`ui-router` documentation](https://github.com/angular-ui/ui-router/wiki)
* State
  * Child states
  * `$stateProvider.state()`
* Templates
  * Inline templates (`template: '<h1>So easy!</h1>'`)
  * Separate files (`templateUrl: 'myTemplate.html'`)
* `ui-view` directive

### NPM
* `package.json`
  * [`package.json`: An Interactive Guide](http://browsenpm.org/package.json)
  * Metadata
  * `devDependencies`
  * Scripts (`npm start`, etc.)
* `node_modules` folder

### Bower
* [What's So Great About Bower?](https://css-tricks.com/whats-great-bower/)
* [Managing Your Front-End Dependencies with Bower](http://zellwk.com/blog/bower/)
* `bower.json`
  * Metadata
  * `dependencies`
* `bower_components` folder

### [Bootstrap](http://getbootstrap.com/)
* [Grid system](http://getbootstrap.com/css/#grid)
* [Button styles](http://getbootstrap.com/css/#buttons)

## Angular Reference

### Concepts
* [Modules](https://docs.angularjs.org/guide/module) ([`angular.module('moduleName', [])`](https://docs.angularjs.org/api/ng/function/angular.module))
* [Controllers](https://docs.angularjs.org/guide/controller) (`someModule.controller('ControllerName', function)`)
* [Scope/`$scope`](https://docs.angularjs.org/guide/scope)

### Directives

{{% notice note %}}
In the view (HTML), directives are specified with **kebab-case** (or "dasherized")—that is, with words separated by hyphens. Within JavaScript, they are specified with **camelCase**.
{{% /notice %}}

* [ngApp](https://docs.angularjs.org/api/ng/directive/ngApp): Auto-bootstraps an Angular application and (optionally) specifies the root Module.
* [ngController](https://docs.angularjs.org/api/ng/directive/ngController): Attaches a Controller to the view/DOM.
* [ngModel](https://docs.angularjs.org/api/ng/directive/ngModel): Binds a form field to a property on the scope.
* [ngRepeat](https://docs.angularjs.org/api/ng/directive/ngRepeat): Repeat an element for each item in a collection.
  * See also: [ngRepeat:dupes](https://docs.angularjs.org/error/ngRepeat/dupes) and `track by`
* [ngSubmit](https://docs.angularjs.org/api/ng/directive/ngSubmit): Specifies custom behavior (often an invocation of a function property on the scope) when a form is submitted.
  * Automatically prevents default, unless the `action` attribute is set on the form.
* [ngClick](https://docs.angularjs.org/api/ng/directive/ngClick): Specifies custom behavior when an element is clicked.
* [ngShow](https://docs.angularjs.org/api/ng/directive/ngShow): Show an element only when the provided expression is truthy.
* [ngHide](https://docs.angularjs.org/api/ng/directive/ngHide): The inverse of `ngShow`. Only show the element if the provided expression is falsey.

## Projects

* Meganote [source](https://github.com/xternbootcamp16/meganote/tree/8221627de162eb9f139749755f190df72581ea6f) | [live](http://bootcamp16.getfretless.com/meganote/#/notes/)
* Acrobats: [source](https://github.com/xternbootcamp16/acrobats) | [live](http://xternbootcamp16.github.io/acrobats/)
