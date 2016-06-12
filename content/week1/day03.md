+++
date = "2016-06-11T17:12:02-04:00"
next = "/week1/day04"
prev = "/week1/day02"
title = "Day 3: Putting the Pieces Together"
toc = true
weight = 3

+++

<date>Thursday, June 2, 2016</date>

> [Solution to Wednesday's homework: MegaRoster with delete and promote](https://github.com/xternbootcamp16/megaroster-afternoon/tree/dfa5fbf687e0eb39fe6e60837eda35778c7e860a)

## Topics

### Foundation
* The grid system
* Responsive design (changing style based on the window size)
* Check out the [Foundation Cheat Sheet](https://sudheerdev.github.io/Foundation5CheatSheet/)

### Functions as Methods
* Methods calling methods (_e.g._ `megaRoster.addChild` calls `this.buildListItem`)
* Binding: Manually setting the value of `this` with `bind`

### Event Objects
* `currentTarget`: The object on which the event occurred

### DOM Manipulation
* `parentElement`
* `childNodes`
* `firstChild`
* `firstElementChild`
* `insertBefore`

### Project Organization
* When to write a new function
* Avoiding global variables

## Presentations
Presentations have been converted from their original format to play in web browsers.

* <a target="_blank" href="/presentations/week1/03-objects-and-functions">Day 2 Review: Objects and Functions</a>

## Homework: MegaRoster - now with even more mega

Enhance MegaRoster! Make the students editable, and add the ability to move them around in the list.

### Baseline Goal
Add a link that moves the student to the top of the list. Either change the behavior of the existing _promote_ link, or add a new _top_ link.

### Bonus Credit
Add links to move the student up and down the list, one spot at a time.

### Mega Bonus Credit
Disable the _up_ link when the student reaches the top, and disable the _down_ link when the student reaches the bottom.

### Super Mega Bonus Credit
Make the student name editable in place after it's added to the roster.

### Super Mega Bonus Credit Hyper Fighting
Make the student data persistent between page refreshes! That is, keep the students from disappearing every time the page is refreshed.

> **Hint**: Use `localStorage`.

> **Update**: [Solution: Editable MegaRoster](https://github.com/xternbootcamp16/megaroster-afternoon/tree/45eebfa3f35d9d617988d5c647ae737e4db16879)
