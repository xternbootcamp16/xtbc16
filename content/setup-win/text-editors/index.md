+++
date = "2016-06-10T23:40:24-04:00"
next = "/setup-win/ssh"
prev = "/setup-win/nodejs"
title = "Text Editors"
toc = true
weight = 5

+++

**[Atom](https://atom.io/)** is free text editor that's especially well-suited for editing code. It is similar to Sublime Text in many respects, but it's completely free and open source, and it's rapidly improving.

## [Download Atom](https://atom.io/)

{{% notice note %}}
Atom requires .NET Framework 4.5.2, which will install automatically if you do not already have it.
{{% /notice %}}

Microsoft's **[Visual Studio Code](http://code.visualstudio.com/)** is also open source and rapidly improving. If you're a fan of Microsoft's IntelliSense and the like, you might prefer VS Code. I **do not** recommend using full-on Visual Studio for JavaScript projects, as it makes managing file unnecessarily complicated.

If you're used to an IDE, **[WebStorm](http://www.jetbrains.com/webstorm/)** might be more up your alley. Be warned: It's subscription-based, and is $12.90/month, or $129.00 the first year.

I will be using Atom in class, so I can show you themes and plugins that I like if you give it a shot. I haven't spent enough time with VS Code to know many tricks, and I've never used WebStorm.

Whichever editor you use, you'll use it enough that I recommend keeping it in the Dock as well.

## Recommended Packages for Atom

Atom is highly extensible, and there are a few packages that I highly recommend.

* [`linter-eslint`](https://atom.io/packages/linter-eslint) checks for JavaScript errors and style violations on the fly.
* [`language-babel`](https://atom.io/packages/language-babel) adds support for the latest JavaScript features.
* [`react`](https://atom.io/packages/react) adds support for React's JSX language.
* [`file-icons`](https://atom.io/packages/file-icons) shows icons in the sidebar that correspond to the file type.
* [`Sublime-Style-Column-Selection`](https://atom.io/packages/Sublime-Style-Column-Selection) is really handy when you've pasted something in with a bunch of junk at the beginning of each line.
* [`autocomplete-plus`](https://atom.io/packages/autocomplete-plus) and [`atom-ternjs`](https://atom.io/packages/atom-ternjs) combine to do pretty nice autocompletion for JavaScript. TernJS even provides inline documentation for functions.

{{% notice note %}}
Since I'm always asked, I use the `Atom Dark` UI theme, and the `Kobalt` syntax theme (with some personal customizations).
{{% /notice %}}
