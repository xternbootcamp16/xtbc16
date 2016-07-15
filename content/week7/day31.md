+++
date = "2016-07-15T14:40:02-04:00"
next = "/week7/day32"
prev = "/week7/day30"
title = "Day 31: Deployment"
toc = true
weight = 3

+++

<date>Wednesday, July 13, 2016</date>

## Topics

### Deploying a Node App to Heroku
* [Heroku](https://heroku.com/) - Cloud platform/infrastructure as a service
* [Heroku Toolbest](https://toolbelt.heroku.com/) - Command-line tools for Heroku
* [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction)
* [Setting Config Vars on Heroku](https://devcenter.heroku.com/articles/config-vars)

{{% notice tip %}}
On Windows, to get Heroku Toolbelt working with Babun, run `export PATH="$PATH;C:\Program Files (x86)\Heroku\bin"`.
{{% /notice %}}

### Deploying an Angular App to GitHub Pages
* The contents of the `app` directory must be at the top level of your `gh-pages` branch.
* The `bower_components` directory must be in the repository, unless you are not dependent on it (if, for example, you've concatenated all of your third-party JS and CSS files).
* Any compiled/transpiled files (_e.g._ `bundle.js`) must be in the repository.

## Projects

### Meganote Server updates

* [Add ESLint config and fix issues.](https://github.com/xternbootcamp16/meganote-server/commit/f69b296bf8218c65b095114dbbdeddc154f9e77b "Add ESLint config and fix issues.")
* [Add a helpers directory.](https://github.com/xternbootcamp16/meganote-server/commit/6f9eab8014b440b96010795fe7aef06d50cc2015 "Add a helpers directory.")
* [Get port number from ENV.](https://github.com/xternbootcamp16/meganote-server/commit/3c44d7d20ff320bfdb8c3e356a93552e769630d9 "Get port number from ENV.")
* [Do not load dotEnv in production.](https://github.com/xternbootcamp16/meganote-server/commit/b3f3d579158534e3600db163b33537ae5458de40 "Do not load dotEnv in production.")
* [Specify node 6.2.0.](https://github.com/xternbootcamp16/meganote-server/commit/f07ae776b138ac4cbea395605333c145b725e377 "Specify node 6.2.0.")
* [Use ES6 promises with Mongoose.](https://github.com/xternbootcamp16/meganote-server/commit/3ac54f69f8ce8666a0aa4e9a9d7a924846787d4b "Use ES6 promises with Mongoose.")
* [Add PORT to .env.example.](https://github.com/xternbootcamp16/meganote-server/commit/9a683601926073af5c03fa1891ca907ba4552b32 "Add PORT to .env.example.")
* [Simplify login code.](https://github.com/xternbootcamp16/meganote-server/commit/86c763fe4fc8eb5f2f803b840e7a2f87c39660a5 "Simplify login code.")

## Meganote Client updates

* [Set a custom page title for each state.](https://github.com/xternbootcamp16/meganote/commit/2cc856147e851982ecefa31102e48b77791b1e98 "Set a custom page title for each state.")
* [Clear flash messages when exiting a state.](https://github.com/xternbootcamp16/meganote/commit/4a7920837074e03c8eebce9a168fd167191911f3 "Clear flash messages when exiting a state.")
* [Add a spinner, displayed on Sign Up only for now.](https://github.com/xternbootcamp16/meganote/commit/12b335086287f29b2d7d6c5599a7547d754ba6e5 "Add a spinner, displayed on Sign Up only for now.")
* [Use a relative path for sign-up template.](https://github.com/xternbootcamp16/meganote/commit/319aca94243daf7686d65275cb9e74fd55503f39 "Use a relative path for sign-up template.")
* [Redirect to sign-up if notes fail to load.](https://github.com/xternbootcamp16/meganote/commit/6db1a18ac5991da08c13bc30712f446c0d2f644b "Redirect to sign-up if notes fail to load.")
* [Concatenate vendor JS files.](https://github.com/xternbootcamp16/meganote/commit/dbb3cdc256df1c61493ad075dfc12800c20cde65 "Concatenate vendor JS files.")
* [Uglify bundle and vendor JS files.](https://github.com/xternbootcamp16/meganote/commit/da2ed31a159bffddc85780d600fd5f4fabeedd1b "Uglify bundle and vendor JS files.")

## Homework

Get your Meganote Server running on Heroku!
