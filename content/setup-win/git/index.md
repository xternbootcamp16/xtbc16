+++
date = "2016-06-10T23:40:01-04:00"
next = "/setup-win/nodejs"
prev = "/setup-win/command-line"
title = "Git"
toc = true
weight = 3

+++

Babun includes Git source code management, which we'll use throughout class.

## Configuring Git

Git comes pre-configured. You just need to tell it what name and email address it should use to sign code that you've authored. Enter the following commands, substituting your actual name and email address:

```zsh
git config --global user.name "Your Full Name"
git config --global user.email "youremailaddress@example.com"
```

{{% notice tip %}}
**[GitHub Desktop](https://desktop.github.com/)** is a very nice, free graphical interface for Git. Although we'll use Git from the command-line a great deal, we'll also look at how GitHub Desktop can make certain tasks easier.
{{% /notice%}}
