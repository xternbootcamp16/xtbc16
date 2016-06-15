+++
date = "2016-06-15T09:05:23-04:00"
next = "/meganote/04-bootstrap"
prev = "/meganote/02-setup"
title = "Google Fonts"
toc = true
weight = 3

+++

Let's add a pair of fonts from Google to our project. Rather than actually add the font files directly to our project, we'll just hotlink the necessary files from a CDN (Content Delivery Network), since Google so graciously provides one.

Visit [Google Fonts](https://fonts.google.com/) and browse through some of the selections there. You can try each typeface out right on the page. When you find one you like, click the <i class="fa fa-plus-circle gf-red" aria-hidden="true" title="plus"></i> <span class="sr-only">_plus_</span> button.

You'll see a box with _1 Family Selected_ appear at the bottom of the screen. Click that to pull up the details for that typeface. You'll see the embed code right away—the `<link>` tag that you should add to the head of your HTML.

This will be the link for only one style of the typeface in order to keep the download small, and thus _fast_. You may need to add a bold or italic variant, in which case switch to the <span class="gf-tab">Customize</span> tab and select additional styles. When you're finished, switch back to the <span class="gf-tab">Embed</span> tab and grab the `<link>` tag to embed.

For Meganote, I've picked out one [serif](https://en.wikipedia.org/wiki/Serif) font and one sans-serif font: Merriweather and Oxygen, respectively.

Add the stylesheet link just above `app.css` in the header of the index page.

<p class="file">app/index.html</p>
```html
<link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Merriweather:400,300,300italic|Oxygen:400,300,700">
```

Next, add the following rule to the top of `app.css` itself, just to make sure the font link worked.

<p class="file">app/app.css</p>
```css
body {
  font-family: 'Merriweather';
  font-size: 1.5em;
}
```

If you refresh, the body text should appear in a lovely serif font.

Let's commit:

<p class="file">shell</p>
```zsh
git add .
git commit -m "Add Merriweather and Oxygen fonts from Google."
git push
```
