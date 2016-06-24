+++
date = "2016-06-24T15:41:42-04:00"
next = "/week4/day19"
prev = "/week4/day18"
title = "Day 19: Resolve and Directives"
toc = true
weight = 5

+++

<date>Friday, June 24, 2016</date>

## Topics

### [Resolve](https://github.com/angular-ui/ui-router/wiki#resolve)
  * Use resolve to provide your controller with content or data that is custom to the state.
  * Promises will be resolved and converted to a value _before_ the controller is instantiated.
  * `$stateChangeError` - fired when an error occurs during the transition to a state
  * Properties of the resolve object can be injected into the controller for the state.

```js
$stateProvider.state('example', {
  url: '/example',
  controller: 'ExampleController',
  resolve: {
    user: function(authService) {
      return authService.auth.$requireSignIn();
    }
  }
});
```

### [Custom Directives](https://docs.angularjs.org/guide/directive)
  * Angular directives are markers that tell AngularJS to attach specified behavior to a DOM element.
  * Directives can be used in the DOM as an Element, Attribute, Class, or Comment.
  * Use isolate scope to prevent the directive from inheriting from parent scope.
  * Directive names are [camelCase](http://en.wikipedia.org/wiki/CamelCase) in Javascript and [dash-delimited](http://en.wikipedia.org/wiki/Letter_case#Computers) in HTML.

JavaScript
```js
app.directive('myDirective', function() {
  return {
    restrict: 'E',
    scope: {},
    templateUrl: 'app/example.html'
  }
});
```
HTML
```html
<my-directive></my-directive>
```

### More Firebase Authentication
  * `$getAuth()` - synchronously retrieves the current authentication state
  * `$requireSignIn()` - returns the user if authenticated, `AUTH_REQUIRED` error if not
  * [Authenticating with Routers](https://www.firebase.com/docs/web/libraries/angular/guide/user-auth.html#section-routers)

## Homework
Fork the [Meganote Repo](https://github.com/xternbootcamp16/meganote) to your personal GitHub.  Refactor it according to [John Papa's Angular Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md) and submit a pull request on the original repo when you are done.

### Criteria
  * [Singular Responsibility](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#single-responsibility)
  * [IIFE](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#iife)
  * [Bindable members up top](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#bindable-members-up-top)
  * [controllerAs with vm](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#controlleras-with-vm)
  * Use an Angular `.constant` to provide the value of the URL in the requests to the API

### Mega Bonus Credit
Refactor the notes service as a factory

### Super Mega Bonus Credit
Refactor the notes-form as a directive instead of child state

## Project
Mutant Office Hours: [Source](https://github.com/xternbootcamp16/mutant-office-hours/tree/37c3e7df30ff50e4d9d0805ffd9a6136694e0436)
