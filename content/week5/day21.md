+++
date = "2016-06-28T16:32:11-04:00"
next = "/week5/day22"
prev = "/week5/day20"
title = "Day 21: Directives and Angular Form Validation"
toc = true
weight = 2

+++

<date>Tuesday, June 28, 2016</date>

## Topics

### Directives
  * [Creating Custom Directives](https://scotch.io/tutorials/angularjs-form-validation)
  * Binding to isolate scope
    * `=` - two-way data binding
    * `&` - one-way data binding
    * `@` - for binding of strings
  * Use `bindToController` if using `controllerAs` syntax in the directive
  * [AngularJS Directives, Using Isolated Scope with Attributes](https://blog.umur.io/2013/07/02/angularjs-directives-using-isolated-scope-with-attributes/)

Data binding example
```js
angular
  .module('myApp')
  .directive('myDirective', myDirective);

function myDirective() {
  return {
    templateUrl: 'myTemplate.html',
    restrict: 'E',
    scope: {
      example: '='
    }
  };
}
```
```html
<my-directive example="vm.exampleValue"></my-directive>
```


### Angular Form Validation
  * [AngularJS Form Validation](https://scotch.io/tutorials/angularjs-form-validation) - Excellent tutorial by scotch.io
  * Angular form Properties
    * `$valid` - _Boolean_  - Tells if an item is currently valid
    * `$invalid` - _Boolean_ - Opposite of `$valid`
    * `$pristine` - _Boolean_ - True if the item (form or input) has not been used yet
    * `$dirty` - _Boolean_ - True if the item has been used
  * [Angular Documentation for Forms](https://docs.angularjs.org/guide/forms)

### [Foundation Callouts](http://foundation.zurb.com/sites/docs/callout.html)
Easy Foundation classes useful for error rendering

## Homework
We added callouts to display Firebase server errors and "email required" errors on the login form.  Add additional callouts for validating email format and password presence.

## Project
Mutant Office Hours: [Source](https://github.com/xternbootcamp16/mutant-office-hours/tree/fa8a6ca1046213b805b4518ce10dd05a879bb24b)
