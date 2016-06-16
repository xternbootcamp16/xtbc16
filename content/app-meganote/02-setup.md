+++
date = "2016-06-14T22:45:03-04:00"
next = "/app-meganote/03-google-fonts"
prev = "/app-meganote/01-seed"
title = "Setup"
toc = true
weight = 2

+++

## Angular-seed

[Angular-seed](https://github.com/angular/angular-seed) is a bootstrapping project preconfigured to with a suite of tools to make it easy to manage dependencies—including Angular itself—with a directory structure that works well for Angular apps. You could always start a new Angular app from scratch, but using the official seed project is a good idea.

Angular-seed can be a bit overwhelming, because it includes an awful lot of stuff. We'll use our own, considerably simpler seed project, `meganote-seed`.

## Meganote-seed structure

Let's take a look at the generated application structure, and what all the pieces are for:

```
├── LICENSE             --> the MIT license agreement
├── app                 --> all of the source files for the application
│   ├── app.js          --> main application module
│   ├── content         --> static assets, like stylesheets and images
│   │   └── app.css     --> main stylesheet
│   ├── index.html      --> main HTML template for the app
│   └── notes           --> view template and logic for _notes_
│       └── notes.html  --> view template for _notes_
├── bower.json          --> client side dependencies (for `bower install`)
└── package.json        --> development and server side dependencies (for `npm install`)
```

## NPM (`package.json`) and Bower (`bower.json`)

Starting with non-empty `package.json` and `bower.json` files is one of the handiest aspects of starting from a _seed_ project.

> `package.json` and `bower.json` serve much the same purpose in a JavaScript project as the `Gemfile` in a Ruby project (and a bit like the `Rakefile` as well).

[NPM](https://www.npmjs.com/) and [Bower](http://bower.io/) are both package managers. Package managers make the distribution and installation of software dramatically easier than alternative methods. Sometimes we need to reuse the same chunk of code in multiple projects. Sometimes our coworkers need to use software we've written for a previous project in a new project. Sometimes we want to share something we've written with the world. In cases like these, using a package manager can simplify including external dependencies and keeping them up-to-date.

NPM, a package manager based on Node, is the most common package management system in the JavaScript world. NPM dependencies and scripts for a project are specified in the `package.json` file.

Bower is also extremely common and serves a subtly different purpose. Its dependencies and scripts are specified in `bower.json`.

Like other package managers, NPM and Bower provide a standardized structure that we can use to package and distribute software we've written.

Why do we need two package managers in our project? Why can't we use *either* npm or bower, rather than both? npm is ideally suited for managing server-side Node packages and development dependencies—like development-friendly web servers, minification tools, etc.—while Bower is designed for the client side.

The biggest technical difference is that npm handles nested dependencies, while Bower leaves that up to us (which is appropriate for the client side, where we don't want, for example, 5 different versions of jQuery sent to end users).

## `npm start`

We can run a task from the command line called `npm start`, because the `start` script is defined in `package.json`.

```json
  "start": "http-server app -a 0.0.0.0 -p 8000 -c-1",
  "prestart": "npm install",
  "postinstall": "bower install"
}
```

So that `start` script fires up a web server, serving the project's `app` directory, on port `8000`. The `prestart` script will automatically execute `npm start` before the `start` script itself. Similarly, the `postinstall` script will automatically execute `bower install` as soon as `npm install` finishes.

All told, running the following command:

```zsh
npm start
```

Will execute the following commands, in this order:

```zsh
npm install
bower install
http-server app -a 0.0.0.0 -p 8000 -c-1
```

Go ahead and run `npm start` now.

You'll see the `node_modules` and `app/bower_components` directories are added to your project with all the installed dependencies. Don't worry about it adding bloat to your repository. Just like the bundled gems in a Ruby project, `node_modules` and `bower_components` are in `.gitignore`.

> If you don't want other developers on the project to have to re-download the dependencies from the web, you can include the two directories in your repository.

Dependencies are versioned, so if you were to change the version number, and run `npm install` again, bower will get the correct version of whatever dependency we need.

If npm and bower have finished installing dependencies, the output of `npm start` should end with this:

```zsh
Starting up http-server, serving app on port: 8000
Hit CTRL-C to stop the server
```

Visit [http://localhost:8000](http://localhost:8000) in your web browser.

Hopefully you see something like this:

```shell
Meganote

Welcome to Meganote!
```

If so, let's keep moving.
