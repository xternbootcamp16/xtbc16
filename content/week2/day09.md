+++
date = "2016-06-11T23:47:58-04:00"
prev = "/week2/day08"
title = "Day 9: Intro to Angular"
toc = true
weight = 5

+++

<date>Friday, June 10, 2016</date>

## Student Presentations

Group projects demonstrating the use of jQuery, DOM manipulation, and using Ajax to consume REST APIs.

## Topics: Introduction to Angular

### Concepts
* [Model-View-Controller (MVC) design pattern](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)
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
* [ngBind](https://docs.angularjs.org/api/ng/directive/ngBind): Tells Angular to replace the text of the element with the value of an expression. You typically use `{{ expression }}` instead, but `ngBind` prevents the template from being displayed briefly when the page loads. But for that you can also use...
* [ngCloak](https://docs.angularjs.org/api/ng/directive/ngCloak): Prevent the template from displaying before the view is fully rendered.

## Projects

Acrobats: [source](https://github.com/xternbootcamp16/acrobats) | [live](http://xternbootcamp16.github.io/acrobats/)
