+++
date = "2016-06-11T17:32:08-04:00"
next = "/week2"
prev = "/week1/day03"
title = "Day 4: LocalStorage & jQuery"
toc = true
weight = 4

+++

<date>Friday, June 3, 2016</date>

> [Solution to Thursday's homework: Editable MegaRoster](https://github.com/xternbootcamp16/megaroster-afternoon/tree/45eebfa3f35d9d617988d5c647ae737e4db16879)

## Topics

### The DOM
* Editable content: [`contenteditable`](http://blog.teamtreehouse.com/native-rich-text-editing-with-the-contenteditable-attribute)
* [Data attributes and `.dataset`](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes)

{{% notice note %}}
If you want to know more, the above items also link to explanations and tutorials.
{{% /notice %}}

### `localStorage`
* [Using `localStorage`]((https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/))
* `JSON.stringify`
  * [Using `JSON.stringify`](http://www.dyn-web.com/tutorials/php-js/json/stringify.php)
  * [Live example](http://jsfiddle.net/queryj/hLkUz/)
  * [API reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify), including optional arguments for whitelisting properties and transforming the data as it's stringified
* `JSON.parse`
  * [Using `JSON.parse`](http://www.dyn-web.com/tutorials/php-js/json/parse.php)
  * [API reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse), including optional argument for transforming the data as it's parsed

### CSS Selectors
* [`:first-child` pseudo-selector](http://www.w3schools.com/cssref/sel_firstchild.asp)
* [`:last-child` pseudo-selector](http://www.w3schools.com/cssref/sel_last-child.asp)
* [[_attribute_=_value_] selector](http://www.w3schools.com/cssref/sel_attribute_value.asp) (_e.g._ `[contenteditable=true]`)

{{% notice note %}}
Each of the above items links to the [w3schools](http://www.w3schools.com/) page for that selector, including examples, reference material (including browser support) and a _Try it Yourself_ live editor.
{{% /notice %}}

{{% notice tip %}}
w3schools has a thorough [reference of CSS selectors](http://www.w3schools.com/cssref/css_selectors.asp) beyond those we've discussed (or will discuss) in class. **Seriously**, if you're having any trouble with selectors, check out [CSS Diner](http://flukeout.github.io/) and [CSS Selector Game](http://toolness.github.io/css-selector-game/).
{{% /notice %}}

### [Font Awesome](http://fontawesome.io/)
* [Examples](http://fontawesome.io/examples/)
* [Icon list](http://fontawesome.io/icons/)
* [Font Awesome intro](http://www.w3schools.com/icons/fontawesome_icons_intro.asp) on w3schools, including a live editor
* [Icon Fonts &amp; Accessibility](http://fontawesome.io/accessibility/)

### Foundation
* [Button styles](http://foundation.zurb.com/sites/docs/v/5.5.3/components/buttons.html)

> Don't forget your friend the [Foundation Cheat Sheet](https://sudheerdev.github.io/Foundation5CheatSheet/).

### jQuery

> If you're new to jQuery, start with [Try jQuery](https://www.codeschool.com/courses/try-jquery).

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

* <a target="_blank" href="/presentations/week1/04a-localstorage">`localStorage`</a>
* <a target="_blank" href="/presentations/week1/04b-jquery">jQuery</a>

## Projects
* [Megaroster with editable names](https://github.com/xternbootcamp16/megaroster-afternoon/tree/45eebfa3f35d9d617988d5c647ae737e4db16879)

## Homework

Make MegaRoster even fancier!

### Baseline Goal
* Make the student data persistent between page refreshes! That is, keep the students from disappearing every time the page is refreshed. (Use `localStorage`.)

{{% notice tip %}}
You'll want to keep track of the student data—just the data, not the HTML elements—in an array.
{{% /notice %}}

**Solution**: [MegaRoster with localStorage](https://github.com/xternbootcamp16/megaroster/tree/7e826425584aae6ae72f7be20392fe13d5f0743d)

### Bonus Credit
* Make the `edit`, `up`, etc. links look like buttons using Foundation styles.
* Use Font-Awesome to make them even fancier.
* Make it prettier to your heart's content.

**Solution**: [MegaRoster HTML and CSS snippets](http://xternbootcamp16.github.io/megaroster/snippets.html)

### Mega Bonus Credit
* Add a _favorite_ button that changes the appearance of the list item.
* Make sure the _favorite_ status persists between page loads.

**Solution**: Included in [MegaRoster with localStorage](https://github.com/xternbootcamp16/megaroster/tree/7e826425584aae6ae72f7be20392fe13d5f0743d)

### Super Mega Bonus Credit
Convert it to jQuery (ideally in a separate branch). The good news is that jQuery is already available in your project, thanks to Foundation.

**Solution**: [MegaRoster with jQuery](https://github.com/xternbootcamp16/megaroster/tree/jquery)
