+++
date = "2016-06-10T23:40:12-04:00"
next = "/setup-win/text-editors"
prev = "/setup-win/git"
title = "NodeJS"
toc = true
weight = 4

+++

## Installation

The NodeJS web site has a big, green install button. That's all there is to setting up Node.

### [Download NodeJS](http://nodejs.org/)

{{% notice note %}}
Node version numbers are confusing, but you should using either the LTS version (4.4.5 as of this writing) or the Current version (6.2.1).
{{% /notice %}}

## Testing your installation

After Node is installed, close Babun and reopen it. That way, `node` and other related commands will be available to you from any folder. Test your installation by running the following command:

```zsh
npm install -g bower
```

You should see an animated cursor for a moment or two, then something like the following:

```zsh
C:\Users\whoever\AppData\Roaming\npm
`-- bower@1.7.9
```
