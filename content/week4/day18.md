+++
date = "2016-06-23T11:36:04-04:00"
next = "/week4/day19"
prev = "/week4/day17"
title = "Day 18: Re-Factory-ing"
toc = true
weight = 4

+++

<date>Thursday, June 23, 2016</date>

## Topics

### Controllers
  * Should only handle logic that directly relates to the view
  * [Defer Controller Logic to Services](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#accessible-members-up-top)
  * [Making Skinny AngularJS Controllers](https://scotch.io/tutorials/making-skinny-angularjs-controllers) - a well-explained article showing the before and after of refactoring a controller using services

  {{% notice tip %}}
  If code is requesting data from an API or database, it should probably be in a service
  {{% /notice %}}

### Factories
  * Handle the business logic so your controllers can be slim and focused
  * [Single Responsibility](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#single-responsibility-1)
  * [Accessible Members Up Top](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md#accessible-members-up-top) - Similar to 'bindable members up top' for controllers
  * [`angular.service` vs `angular.factory`](http://stackoverflow.com/questions/14324451/angular-service-vs-angular-factory)

Basic Setup of an Angular Factory (IIFE excluded for brevity)

```js
angular
  .module('myModule')
  .factory('myFactory', myFactory);

function myFactory() {
  var service = {};

  return service;
}
```

## Homework
  * Review today's commit history
  * We set up the authService factory and created the `register` property on it.  Continue adding additional properties to the factory to refactor the other methods and dependencies in the `AuthController`

## Project
Mutant Office Hours: [Source](https://github.com/xternbootcamp16/mutant-office-hours/tree/699f1bce23c4209ad93b0ec415b3fd30100b3c1b)
