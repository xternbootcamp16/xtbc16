+++
date = "2016-06-10T23:16:25-04:00"
next = "/setup-mac/text-editors"
prev = "/setup-mac/git"
title = "NodeJS"
toc = true
weight = 4

+++

## Installation
If you installed Homebrew in the previous step, use it to install NodeJS:

```zsh
brew install node
```

If not, you can click the big, green *INSTALL* button on the NodeJS web site.

### [Download NodeJS](http://nodejs.org/)

{{% notice note %}}
Node version numbers are confusing, but you should using either the LTS version (4.4.5 as of this writing) or the Current version (6.2.1).
{{% /notice %}}

## Testing your installation

After Node is installed, test your installation by running the following command:

```zsh
npm install -g bower
```

You should see an animated cursor for a moment or two, then something like the following:

```zsh
/usr/local/bin/bower -> /usr/local/lib/node_modules/bower/bin/bower
/usr/local/lib
└── bower@1.7.9
```

{{% notice tip %}}
If the `npm` command isn't available, open a new tab in Terminal or iTerm2 and try again. Opening a new tab should make `node` and other related commands available to you from any directory, if they weren't already.
{{% /notice %}}
