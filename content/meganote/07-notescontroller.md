+++
date = "2016-06-15T19:53:04-04:00"
next = "/meganote/07-notescontroller"
prev = "/meganote/06-modules-routes"
title = "NotesController"
toc = true
weight = 5

+++

Inject a dependency for the `Notes` module/controller that we'll soon create, and update the catch-all route:

_app/app.js_
```javascript
angular.module('meganote', [
...
  'meganote.version',
  'meganote.notes'
...
  $routeProvider.otherwise({redirectTo: '/notes'});
...
```

Make a new directory for our new module, `app/notes`, and add a file named `notes.js` under it:

_app/notes/notes.js_
```javascript
'use strict';

angular.module('meganote.notes', ['ngRoute'])

.config(['$routeProvider', function($routeProvider) {
  $routeProvider.when('/notes', {
    templateUrl: 'notes/notes.html',
    controller: 'NotesController'
  });
}])

.controller('NotesController', [function() {

}]);
```

Add a file `app/notes/notes.html`:

_app/notes/notes.html_
```html
Welcome to Meganote.
```

Specifying the dependencies to AngularJS is not sufficient to actually get those scripts sent to browsers. We must require the notes controller in `index.html`:

_app/index.html_
```html
  <script src="notes/notes.js"></script>
```

Now, if you visit the root url (http://localhost:8000/), you should be taken to `/notes` and see the welcome message from `app/notes/notes.html`.

Commit.
