+++
date = "2016-06-14T21:56:25-04:00"
next = "/meganote/02-setup"
prev = "/meganote"
title = "Meganote-Seed"
toc = true
weight = 1

+++

## Clone the [meganote-seed](https://github.com/xternbootcamp16/meganote-seed) project

Clone the seed project in a local folder named `meganote`.

```zsh
git clone git@github.com:xternbootcamp16/meganote-seed.git meganote
cd meganote
```

## Remove its `.git` history, and initialize your own git repository

Open the project in Atom and delete the `.git` folder to remove all traces of the seed project's repository.

Then initialize your own repository.

```zsh
git init
git add .
git commit -m "Initial commit using meganote-seed"
```

### Note About Commit Messages

If you fail to specify a commit message, git will open a text editor for you to write the message manually. By default, it opens `vim`, a powerful, but sometimes confusing terminal-based text editor.

To configure Git to use Atom instead, type the following command:

```zsh
git config --global core.editor "atom --wait"
```

## Create a GitHub repo

Create a new repository in your GitHub account. Follow the instructions to add this repo as a remote for your local project, and push to that remote.

```zsh
git remote add origin git@github.com:[YOUR GITHUB USERNAME]/meganote.git
git push -u origin master
```
