+++
date = "2016-06-11T23:34:13-04:00"
next = "/week2/day07"
prev = "/week2/day05"
title = "Day 6: More Ajax"
toc = true
weight = 2

+++

<date>Tuesday, June 7, 2016</date>

## Topics

### Ajax
* Check out [Ajax with jQuery: A Beginner's Guide](http://www.elated.com/articles/ajax-with-jquery-a-beginners-guide/);
* [GET vs. POST](http://www.w3schools.com/tags/ref_httpmethods.asp)

### CDNs
* [Why use a CDN?](http://stackoverflow.com/a/2180401)
* [CDNjs](https://cdnjs.com/)
* [jQuery 2.2.4 on CDNjs](https://cdnjs.com/libraries/jquery/2.2.4)

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>
```

## Presentations
Presentations have been converted from their original format to play in web browsers.

* <a target="_blank" href="/presentations/week2/06-ajax-get-requests-and-github-pages-review">Ajax - GET requests in detail, GitHub pages review</a>

## Projects
* jMutants: [morning](https://github.com/xternbootcamp16/jmutants-afternoon) (with working _edit_ feature) | [afternoon](https://github.com/xternbootcamp16/jmutants-afternoon) (without edit, but with _mutant name_, _real_name_, and _power_)

## Links
* [Astronomy Picture of the Day](https://api.nasa.gov/api.html#apod)

```js
$.get({
  url: 'https://api.nasa.gov/planetary/apod',
  data: {
    API_KEY: 'DEMO_KEY',
    date: '2016-06-07'
  }
  success: function(data) {
    $(document.body).prepend('<img src="' + data.hdurl + '">');
  }
});
```

{{% notice note %}}
If you plan to do much with the NASA APIs, you'll need to sign up for your own API_KEY, which is free.
{{% /notice %}}

## Homework

Try to get further with yesterday's homework.

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
Add [Pok&eacute;mon](https://pokeapi.co/docsv2/#pokemon), [Star Wars characters](https://swapi.co/documentation), or something else with an existing API.
