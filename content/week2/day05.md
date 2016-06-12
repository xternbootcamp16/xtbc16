+++
date = "2016-06-11T23:23:36-04:00"
next = "/week2/day06"
prev = "/week2"
title = "Day 5: jQuery & Ajax"
toc = true
weight = 1

+++

<date>Monday, June 6, 2016</date>

## Topics

### Deployment
* [Deploying to GitHub Pages](https://pages.github.com/)

```zsh
git checkout -b gh-pages     # Create a new branch
git push -u master gh-pages  # Push it to GitHub
```

Your site will be published at _username_.github.io/_repository_.

### Ajax
* [`jQuery.ajax()`](http://api.jquery.com/jQuery.ajax/)
  * [w3schools page and _Try It Yourself_ demo](http://www.w3schools.com/jquery/ajax_ajax.asp)
* [JSONP](http://stackoverflow.com/questions/3839966/can-anyone-explain-what-jsonp-is-in-layman-terms)

### JavaScript Arrays
* [Array `map()`](http://www.w3schools.com/jsref/jsref_map.asp)
* [Array `splice()`](http://www.w3schools.com/jsref/jsref_splice.asp)

{{% notice note %}}
Each of the above items links to the [w3schools](http://www.w3schools.com/) page for that method, including examples, reference material (including browser support) and a _Try it Yourself_ live editor.
{{% /notice %}}

### CSS Selectors
* [`:hover` pseudo-class](http://www.w3schools.com/cssref/sel_hover.asp)
* [[_attribute_=_value_] selector](http://www.w3schools.com/cssref/sel_attribute_value.asp) (_e.g._ `[data-id=4]`)

{{% notice tip %}}
> **Seriously**, if you're having any trouble with selectors, check out [CSS Diner](http://flukeout.github.io/) and [CSS Selector Game](http://toolness.github.io/css-selector-game/).
{{% /notice %}}

### jQuery

{{% notice tip %}}
If you're new to jQuery, start with [Try jQuery](https://www.codeschool.com/courses/try-jquery).
{{% /notice %}}

* [`$()`, the jQuery function](http://api.jquery.com/jquery/)
* [Selecting elements](https://learn.jquery.com/using-jquery-core/selecting-elements/)
* [jQuery Objects vs. DOM elements](https://learn.jquery.com/using-jquery-core/jquery-object/)
* [Manipulation](https://learn.jquery.com/using-jquery-core/manipulating-elements/)
* [DOM traversal](https://learn.jquery.com/using-jquery-core/traversing/)
* [Events](https://learn.jquery.com/events/)
* More jQuery tutorials:
  * [Codecademy's Intro to jQuery](https://www.codecademy.com/en/courses/web-beginner-en-bay3D/resume?curriculum_id=50a3fad8c7a770b5fd0007a1)
  * [jQuery Tutorial on w3schools](http://www.w3schools.com/jquery/default.asp)

{{% notice note %}}
Be sure to check out the excellent [jQuery API documentation](http://api.jquery.com/).
{{% /notice %}}

## Presentations
Presentations have been converted from their original format to play in web browsers.

* <a target="_blank" href="/presentations/week2/05-ajax-and-github-pages">GitHub Pages, jQuery, and Ajax</a>

## Projects
* [MegaRoster with localStorage](https://github.com/xternbootcamp16/megaroster)
* [MegaRoster with jQuery](https://github.com/xternbootcamp16/megaroster/tree/jquery)
* [MegaRoster with Ajax](https://github.com/xternbootcamp16/megaroster/tree/ajax)
* MegaRoster with mutants: [source](https://github.com/xternbootcamp16/megaroster/tree/mutants) | [live](http://xternbootcamp16.github.io/megaroster/)
* JSON People: [source](https://github.com/xternbootcamp16/json-people) | [live](http://xternbootcamp16.github.io/json-people/)

## Links
* [Astronomy Picture of the Day](https://api.nasa.gov/api.html#apod)

```js
$.ajax({
  url: 'https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY',
  method: 'get',
  success: function(data) {
    $(document.body).prepend('<img src="' + data.hdurl + '">');
  }
});
```

## Homework

Talk to the [Mutant School API]((http://getfretless.github.io/mutant-school-docs/?javascript#get-a-specific-mutant))!

### Baseline Goal
* Start a new project (or fork JSON People and work from there) that loads all Mutants from the API.
* When a new record is added to your app, create a new Mutant record by POSTing to the API.

### Bonus Credit
Add a button to delete individual mutants from the API.

### Mega Bonus Credit
Update existing mutant records.

### Super Mega Bonus Credit
Integrate the Mutant API with MegaRoster.

### Super Mega Bonus Credit Hyper Fighting
Add [Pok&eacute;mon](https://pokeapi.co/docsv2/#pokemon), [Star Wars characters](https://swapi.co/documentation), or something else from an existing API.
