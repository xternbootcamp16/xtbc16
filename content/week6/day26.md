+++
date = "2016-07-06T14:18:59-04:00"
next = "/week6/day26"
prev = "/week6/day25"
title = "Day 26: Gulp"
toc = true
weight = 2

+++

<date>Wednesday, July 6, 2016</date>

## Topics

### [Gulp](http://gulpjs.com/)
  * A JavaScript task runner that lets you automate repetitive tasks such as:
    * Concatenating JS files
    * Refreshing the browser when a file is saved
    * Bundling and minifying files
    * Running unit tests
    * And so much more!
  * [What is Gulp.js and why use it?](http://brandonclapp.com/what-is-gulp-js-and-why-use-it/)
  * [Quick intro to Gulp.js](https://www.codefellows.org/blog/quick-intro-to-gulp-js)

### Basic Setup

First, install Gulp globally if you don't already have it on your machine
```sh
npm install -g gulp
```

Use `npm install` to add Gulp and other plugins that you need to the dev dependencies of your project in `package.json`
```sh
npm install --save-dev gulp gulp-concat gulp-plumber gulp-babel
```

Add `gulpfile.js` at the root level of your project and add references to the node modules you installed
```js
var gulp = require('gulp');
var concat = require('concat');
var plumber = require('plumber');
var babel = require('babel');
```
And now you're ready to start writing Gulp tasks!

### Gulp plugins used in Meganote (so far...)
  * [`gulp-concat`](https://www.npmjs.com/package/gulp-concat) - Concatenates files
  * [`gulp-sourcemaps`](https://www.npmjs.com/package/gulp-sourcemaps) - Maps concatenated / minified files back to original sources
  * [`gulp-plumber`](https://www.npmjs.com/package/gulp-plumber) - Prevent pipe breaking caused by errors from Gulp plugins
  * [`gulp-babel`](https://www.npmjs.com/package/gulp-babel) - Transpile ES6 to ES5
  * [`gulp-connect`](https://www.npmjs.com/package/gulp-connect) - Run a webserver with live reloading
  * [`gulp-order`](https://www.npmjs.com/package/gulp-order) - Order a stream of files

## Projects
Meganote: [Morning](https://github.com/xternbootcamp16/meganote/tree/4cde223e83105c2a49530161a1a9779aaecbaad8) | [Afternoon](https://github.com/xternbootcamp16/meganote/tree/8f13a322ccafd0afa43146f1229c387cd737c358)

Meganote-server: [Source](https://github.com/xternbootcamp16/meganote-server/tree/a8125a986c42db2308a5559ebad84e72559eca3e)
