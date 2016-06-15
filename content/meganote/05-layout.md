+++
date = "2016-06-15T15:39:05-04:00"
next = "/meganote/06-modules-routes"
prev = "/meganote/04-bootstrap"
title = "Layout & Style"
toc = true
weight = 5

+++

Now that we have Bootstrap and font stuff in place, let's start to make this look like a real app.

Our app content gets inserted inside `<div ui-view></div>` (more on that later), so we'll put some basic structure around that using Bootstrap's grid system.

{{% notice note %}}
Read all about [Bootstrap's grid system](http://getbootstrap.com/css/#grid) in the official documentation for [Bootstrap's CSS](http://getbootstrap.com/css/).
{{% /notice %}}

When we're done, our `index.html` should look like this:

<p class="file">app/index.html</p>
```html
<!DOCTYPE html>
<!--[if lt IE 7]>      <html lang="en" ng-app="meganote" class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html lang="en" ng-app="meganote" class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html lang="en" ng-app="meganote" class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!--> <html lang="en" ng-app="meganote" class="no-js"> <!--<![endif]-->
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title ng-bind="$state.current.name + ' - Meganote'">Meganote</title>
    <link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Merriweather:400,300,300italic|Oxygen:400,300,700">
    <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="/content/app.css" charset="utf-8">
  </head>
  <body>

    <div class="container wrap">
      <div class="row">
        <div class="col-xs-12">
          <header>
            <div class="well">
              Meganote
            </div>
          </header>
        </div>
      </div>
      <div ui-view></div>
    </div>


    <script src="bower_components/jquery/dist/jquery.min.js"></script>
    <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
    <script src="bower_components/angular-loader/angular-loader.min.js"></script>
    <script src="bower_components/angular/angular.min.js"></script>
    <script src="bower_components/angular-ui-router/release/angular-ui-router.min.js"></script>
    <script src="app.js"></script>
  </body>
</html>
```

Now update `app.css` with some nice styles:

<p class="file">app/content/app.css</p>
```css
body {
  font-family: Oxygen, Helvetica, Arial, sans-serif; }

h1, h2, h3, h4, h5 {
font-family: Merriweather;
font-weight: 300;
color: #FE5F55; }

.container {
  width: 100% !important;
  padding-left: 0 !important;
  padding-right: 0 !important; }

.row {
  margin-left: 0 !important;
  margin-right: 0 !important; }

.col-xs-12 {
  padding-left: 0 !important;
  padding-right: 0 !important; }

header .well {
  padding-top: 5px;
  padding-bottom: 5px; }
  header .well .user-links {
    float: right;
    color: #ccc; }
    header .well .user-links a {
      cursor: pointer; }

a:link, a:visited, a:hover, a:active {
  color: #FE5F55; }

i.fa-trash-o {
  color: #ccc;
  font-size: 150%;
  vertical-align: middle;
  margin-left: 1em; }
  i.fa-trash-o:hover {
    color: #999; }

.wysihtml5-toolbar .btn-default {
  color: #999; }

input#note_title {
  border: none;
  font-size: 200%;
  font-family: Merriweather;
  color: #FE5F55;
  font-weight: 300;
  width: 100%; }
  input#note_title:focus {
    outline: none; }

ul#notes {
  list-style: none;
  margin-top: 1em;
  padding: 0;
  width: 100%;
  color: #999; }
  ul#notes li {
    border-top: 1px solid #ddd;
    height: 100px;
    font-size: 90%;
    cursor: pointer;
    overflow: hidden; }
    ul#notes li:first-of-type {
      border-top: none; }
    ul#notes li:hover {
      color: white;
      background-color: #FE5F55; }
      ul#notes li:hover .note-title {
        color: white; }
    ul#notes li .note-title {
      color: black;
      font-family: Merriweather;
      font-size: 120%;
      font-weight: 300; }
    ul#notes li .note-body {
      height: 54px;
      overflow: hidden; }
    ul#notes li a.note {
      display: block;
      height: 100px;
      padding: 1em;
      text-decoration: none; }
    ul#notes li a.note:hover {
      color: white; }

#new_user input[type="text"],
#new_user input[type="password"] {
  width: 300px;
  font-size: 120%;
  border-radius: 4px;
  border: 1px solid #ccc;
  padding: 0.25em; }

#welcome h1 {
  color: #FE5F55; }
#welcome main {
  margin: 0 auto;
  width: 360px; }

span.login {
  margin-left: 1em; }

.ta-editor {
  margin-top: 0.5em; }
```

Commit your work:

<p class="file">shell</p>
```zsh
git add .
git commit -m "Add layout and styles"
git push
```
