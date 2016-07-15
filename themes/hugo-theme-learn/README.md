# Xtern Bootcamp 2016 Site

The xtbc16 site was built with [Hugo](http://gohugo.io/), using the [Learn theme](http://themes.gohugo.io/hugo-theme-learn/).

## Running in development

Start the server with the following command:

```shell
hugo serve
```

You can reach the site at [http://localhost:1313](http://localhost:1313). The server features hot-reloading.

## Adding a section

```shell
hugo new --kind chapter path/index.md
```

## Adding a page

```shell
hugo new path/file.md
```

## Building and Deploying

Build the site with the following command:

```shell
hugo
```

The compiled site will be in the `public` directory. Copy its contents to the static host of your choice, or to the `gh-pages` ([GitHub Pages](https://pages.github.com/)) branch.
