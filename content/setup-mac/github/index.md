+++
date = "2016-06-10T23:31:46-04:00"
next = "/setup-mac/mongodb"
prev = "/setup-mac/ssh"
title = "GitHub"
toc = true
weight = 7

+++

## Create a free GitHub account

GitHub is a service for storing your code in the cloud. It's wonderful for collaboration.

[Sign up for GitHub](https://github.com) using the same email address you used when creating your SSH key and your Git configuration.

![Sign up for GitHub with your email address](http://davestrus.com/images/github-01-signup.png)

On the next screen, you'll see information about GitHub's free and paid plans. To finish creating a free account, just hit the green "Finish sign up" button.

![Hit the green "Finish sign up" button.](http://davestrus.com/images/github-02-free.png)

## Add your public key to your GitHub account

To send and receive code between your laptop and GitHub securely, you'll need to add your public SSH key to your GitHub account. **Never copy your private key to another machine unless you are absolutely sure what you're doing.**

Copy the contents of your public key to the clipboard with the following command:

```zsh
cat ~/.ssh/id_rsa.pub | pbcopy
```

> The `cat` command prints the contents of a text file to the screen—or more accurately, to STDOUT. The `pbcopy` command—which is not a standard UNIX utility, but is included with OS X—copies text to the clipboard. The pipe `|` takes the output from the command on the left and passes it as an argument to the command on the right.

Now go to GitHub settings to add your public key to your account.

![Click the settings icon in the upper-right of your GitHub page](http://davestrus.com/images/github-03-settings.png)

Choose "SSH Keys" from the left menu, then click "Add SSH key" on the right.

![Click the button to add an SSH key to your account](http://davestrus.com/images/github-05-add-key.png)

Give your SSH Key a name (something to identify the machine on which the key was generated, such as "MacBook"), and then paste in the contents that you copied from Atom.

![Paste in the contents of your public key](http://davestrus.com/images/github-06-key-details.png)

## Test your SSH key with your GitHub account

Return to Terminal and type the following command:

```zsh
ssh -T git@github.com
```

If all is well, you should see a message like this:

```shell
You've successfully authenticated, but GitHub does not provide shell access.
```

If you see that message, you're in good shape!
