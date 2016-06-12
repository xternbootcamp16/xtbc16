+++
date = "2016-06-10T23:28:03-04:00"
next = "/setup-mac/github"
prev = "/setup-mac/text-editors"
title = "SSH"
toc = true
weight = 6

+++

I recommend setting up an SSH key to simplify authentication with GitHub and other services.

## Check for an existing key

Make sure you're in your home directory. You should be by default, but you can double-check with the "print working directory" command: `pwd`

```zsh
pwd
```

You should be in `/Users/yourusername`. If not, you can switch to that directory with the `cd` command, passing in the directory you want to switch to.

```zsh
cd ~
```

{{% notice tip %}}
You can always use a tilde `~` as a shortcut for your home directory.
{{% /notice %}}

Check to see if you already have an .ssh key configured:

```zsh
ls ~/.ssh/id_rsa
```

If it prints `/Users/yourusername/.ssh/id_rsa`, then you already have an SSH key and can skip to the next page: [[GitHub|06 GitHub]].

## Generate an SSH key

Type the following command to generate your SSH key, substituting the same email address you used for Git earlier:

```zsh
ssh-keygen -t rsa -C "youremail@example.com"
```

It should prompt you for a file name. You can just hit 'enter' to accept the default.

It will then prompt you for a password. You can just hit 'enter' (twice) to not set a passphrase. That compromises your key should anyone gain access to your laptop, but it may be simpler for the sake of this course. It's much safer to use a passphrase when generating a key when you truly want to maximize security.

If all is well, you should see that your identification and your public key have been saved to `.ssh/id_rsa` and `.ssh/id_rsa.pub` respectively.

Run the following command to add your new key to the SSH agent on your Mac:

```zsh
ssh-add ~/.ssh/id_rsa
```

You'll test your new key shortly, but first you'll need to create a GitHub account and add your public key to the account.
