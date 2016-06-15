+++
date = "2016-06-15T15:53:23-04:00"
next = "/meganote/07-notescontroller"
prev = "/meganote/05-layout"
title = "Modules & Routes"
toc = true
weight = 6

+++

Wow. How have we gone this far without looking at `app.js` in any real detail?

<p class="file">app/app.js</p>
```js
(function() {
  var app = angular.module('meganote', [
    'ui.router'
  ]);

  function config($stateProvider, $urlRouterProvider) {
    $urlRouterProvider.otherwise('/notes');

    $stateProvider

      .state('notes', {
        url: '/notes',
        template: '<h1>Meganote</h1><p>{{ message }}</p>',
        controller: function($scope) {
          $scope.message = "Welcome to Meganote!";
        }
      });
  }

  config['$inject'] = ['$stateProvider', '$urlRouterProvider'];
  app.config(config);
})();
```

Now let's break it down.

## angular.module()

This file defines the main Angular module and routing instructions.

The first argument to `angular.module` is the name of the module, and the second argument is an array containing the _names_ of other modules that this one requires, as strings.

{{% notice tip %}}
Without the second argument, you are _retrieving_ an existing module, rather than _creating_ one. Read more on [w3schools](http://www.w3schools.com/angular/angular_modules.asp) or [the official `angular.module` documentation](https://docs.angularjs.org/api/ng/function/angular.module).
{{% /notice %}}

<!-- {{% notice note %}}
Read [AngularJS Dependency Injection Demystified](http://anandmanisankar.com/posts/angularjs-dependency-injection-demystified/) for more information, but rest assured that we'll be coming back to this topic.
{{% /notice %}} -->

The `meganote` module is already setup to require the `ui-router` module, which is also sourced with a `<script>` tag in the layout.

{{% notice note %}}
Since this module represents our entire app, it is the one referenced by the `ng-app` directive on the `<html>` tag in the layout.
{{% /notice %}}

We're saving the new module to a local variable called `app`. Below that, we define a function named `config` that, as its name suggests, will configure our module. This function has two parameters, `$stateProvider` and `$urlRouterProvider`, but of which are services in the UI-Router.

## UI-Router

[UI-Router](https://github.com/angular-ui/ui-router/wiki) is one of several routing frameworks for Angular. Routing frameworks are responsible for managing the URLs in single-page applications like this one. Strictly speaking, we'll always be on `index.html`, but the URL will change as we click around in our app.

UI-Router uses a [_state-machine_](https://en.wikipedia.org/wiki/Finite-state_machine) to manage all of this, so we'll define _states_ that map specific URLs to specific templates and controllers, as well to define some behavior.

{{% notice note %}}
Check out the [UI-Router project page](https://github.com/angular-ui/ui-router) and the [In-Depth Guide](https://github.com/angular-ui/ui-router/wiki) for more information.
{{% /notice %}}

### $stateProvider

We use `$stateProvider` to define states, which can be as simple as giving the state a name and a template.

```js
$stateProvider.state('mutants', {
  template: '<h1>Behold, Ye Mutants!</h1>'
});
```

We could then link to this state from our HTML, despite having not defined a URL for it. Most of the time, however, we will define a URL&emdash;both for the sake of maintaining browser history (_i.e._ preserving the behavior of the _back_ button), and to create direct links to individual resources.

We go one step further and specify a _controller_ as well. The controller is a function that will run whenever this state is loaded.

```js
$stateProvider.state('notes', {
  url: '/notes',
  template: '<h1>Meganote</h1><p>{{ message }}</p>',
  controller: function($scope) {
    $scope.message = "Welcome to Meganote!";
  }
});
```

### $urlRouterProvider

[`$urlRouterProvider`](http://angular-ui.github.io/ui-router/site/#/api/ui.router.router.$urlRouterProvider) watches for changes in the URL and looks for a state with a matching rule.

`$urlRouterProvider.otherwise()` lets us specify a path to use when no matching rule is found. For our app, a reasonable default would be a **notes** page, hence `$urlRouterProvider.otherwise('/notes')`.
