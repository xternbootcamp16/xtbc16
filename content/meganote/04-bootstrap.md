+++
date = "2016-06-15T15:19:00-04:00"
next = "/meganote/05-layout"
prev = "/meganote/03-google-fonts"
title = "Bootstrap"
toc = true
weight = 4

+++

Now that we've committed our basic, empty project, let's add [Bootstrap](http://getbootstrap.com/) to bring some basic structure and mobile-friendly features to our HTML and CSS.

We could download all the bootstrap components manually and include them our project, but we've used some [Bower](http://bower.io/) power to do it for us.

Let's get some info about Bower's Bootstrap package.

<p class="file">shell</p>
```zsh
node_modules/.bin/bower info bootstrap
```

This shows us a bunch of details about that package, including available versions, the exact name of the package (it's just _bootstrap_), and its dependencies. If we install Bootstrap in our project, its dependencies will automatically be installed with it.

To include Bootstrap in our project, we need to list Bootstrap among our dependencies in `bower.json`. The _meganote-seed_ project already included it.

<p class="file">bower.json</p>
```javascript
    "bootstrap": "3.3.6"
```

Had we just added it, we would need to run `bower install` again to actually add the files to our project. Running `npm install` will kick of `bower install` for us, as will just starting up our server with `npm start`.

We still need to include Bootstrap's JavaScript and CSS to our app's home page. Open `app/index.html`, and add the Bootstrap stylesheets and scripts.

Add Bootstrap's stylesheet just above `app.css`, and add the JavaScript just above the other `<script>` tags near the bottom of the `<body>`.

<p class="file">app/index.html</p>
```html
...
  <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.min.css">
  <link rel="stylesheet" href="app.css">
...
  <script src="bower_components/jquery/dist/jquery.min.js"></script>
  <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
</head>
```

If you ever need to update a dependency, all you should need to do is issue:

```zsh
./node_modules/.bin/bower update bootstrap
```

And it will update `bower.json` for you and install the new packages. Provided the paths to assets don't change, you shouldn't need to update your `index.html` file.

{{% notice tip %}}
**Note:** By including `./node_modules/bin/` in that command, we ensure that we are running the version of Bower that's installed in this app. You can omit the path if you have Bower installed globally, which you can do with `npm install -g bower`.
{{% /notice %}}

If you save and refresh the page, you should see some padding that wasn't there before, as well as a change in font sizes.

Let's add everything we've done so far to git and commit again:

<p class="file">shell</p>
```zsh
git add .
git commit -m "Add Bootstrap."
git push
```
