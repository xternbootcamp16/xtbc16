+++
date = "2016-07-14T14:49:51-04:00"
next = "/week7/day32"
prev = "/week7/day30"
title = "Day 32: Minification, Promises and ng-Resource"
toc = true
weight = 4


+++

<date>Thursday, July 14, 2016</date>

## Topics

### Minification
Minification is the process of making code as compact as possible without changing its functionality.  Since a lot of the white space, new lines, descriptive names, comments, and sometimes even block delimiters are purely for human readability, much of it can be stripped out while remaining completely functional.

This is particularly important for JavaScript, since it is served over an internet connection, and the size of the files can dramatically effect the time it takes to transfer the required files and ultimately render a page.  In our project, we used [gulp-uglify](https://www.npmjs.com/package/gulp-uglify) for minifying JavaScript, and [gulp-clean-css](https://www.npmjs.com/package/gulp-clean-css) to minify CSS.

```js
// regular code

var numberArray = [];
for (var i = 0; i < 20; i++ ) {
  numberArray[i] = i;
}

// minified code

var a=[];for(var i=0;i<20;i++){a[i]=i;}

```

### Promises
Promises provide an easy-to-use interface for handling asynchronous tasks without blocking execution while waiting for the async task to complete.  Previously, this type of work was done using callback functions, but nested callbacks can quickly become very difficult to manage (and even read).

Luckily, ES6 now provides native support for promises, so we no longer have to bring in an external promise library to take advantage of them. Basically, promises allow us to use `.then()` functions to write what we would _like to do_ if the promises resolve successfully, and `.catch()` to handle what happens if an error occurs and we don't get the data we expect.

```js

// make a promise
let samplePromise = new Promise((resolve, reject) => {
  if ( /* everything works as we expect */ ) {
    resolve('Great success!')
  } else {
    reject('That did not work...')
  }
})

// use the promise
samplePromise
  .then(result => {
    console.log(result); // 'Great success!'
  })
  .catch(err => {
    console.log(err); // 'That did not work...'
  });

```

Another great thing about promises is that they can be chained together - multiple `.then()` functions can happen sequentially, with each `.then()` depending on the successful return of the promise before it.  An error at any point of the chain propagates through the entire chain, so only one `.catch()` is needed to handle multiple possible errors.

```js
// chained promises
firstPromise
  .then(firstResult => {
    return secondThingThatReturnsAPromise(firstResult);
  })
  .then(secondResult => {
    return thirdThingThatReturnsAPromise(secondResult);
  })
  .then(thirdResult => {
    // do something with thirdResult
  })
  .catch(err => {
    // catches any error from any of the previous promises
  })
```

#### Resources for learning more about Promises
  * [Promises/A+](https://promisesaplus.com/) - the actual specification
  * [JavaScript Promise API](https://davidwalsh.name/promises) - a helpful article about the basics of promises by David Walsh
  * [JavaScript Promises: There and Back Again](http://www.html5rocks.com/en/tutorials/es6/promises/) - A bit more in-depth look by Jake Archibald

### [ngResource](https://docs.angularjs.org/api/ngResource/service/$resource)
`ngResource` is an Angular module that provides interaction support with RESTful services through the `$resource` service (it's a factory). By default, `$resource` provides support for the following actions:

```js
{ 'get':    {method:'GET'},
  'save':   {method:'POST'},
  'query':  {method:'GET', isArray:true},
  'remove': {method:'DELETE'},
  'delete': {method:'DELETE'} };
```

Custom actions can be added when the resource is created by passing additional parameters.

`$resource(url, [paramDefaults], [actions], options);`

## Homework
Create your own Angular app from scratch that utilizes `$resource` to interact with data from an API
