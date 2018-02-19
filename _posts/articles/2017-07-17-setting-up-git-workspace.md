---
layout: post
title: "Setting up a git workspace"
excerpt: "Instructions for setting up your git workspace."
categories: articles
tags: [git, docs]
comments: true
share: true
modified: 2017-07-17
---

This is a look at how to set up your terminal to make it easier to work with Git. These instructions are based on the material from Udacity's [How to Use Git and GitHub](https://classroom.udacity.com/courses/ud775) online course.

## Bash completion support for Git

Save the following file in your home directory with the name `git-completion.bash`. Adding this file provides support for the completion of common Git commands, branch names, and file names among other things when working in the Terminal.

- [Bash completion support](https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash)

## Git prompt support

The following file lets you see the status of your Git repository in your Terminal. For example, your current branch is shown in the prompt.

- Save the [Git prompt support](https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh) file in your home directory with the name `git-prompt.sh`.

## Customizing your command prompt in Terminal

Add the following to the `.bash_profile` file in your home directory. The original file from Udacity can be downloaded [here](https://www.udacity.com/api/nodes/3341718587/supplemental_media/bash-profile-course/download?_ga=1.37232743.672083044.1467344711)

```shell
# Enable tab completion
source ~/git-completion.bash

# colors!
green="\[\033[0;32m\]"
blue="\[\033[0;34m\]"
purple="\[\033[0;35m\]"
reset="\[\033[0m\]"

# Change command prompt
source ~/git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
# '\u' adds the name of the current user to the prompt
# '\$(__git_ps1)' adds git-related stuff
# '\W' adds the name of the current directory
export PS1="$purple\u$green\$(__git_ps1)$blue \W $ $reset"
```

## Restart the terminal

Close and re-open the terminal for the changes to take effect.

## Setting your default editor for Git

The following are instructions for how to set up Visual Studio Code as your default editor for Git.

Run the following command to make VS Code the default editor.

```
git config --global core.editor "code --wait"
```

## Set VS Code as the Git diff tool

Add the following to the `.gitconfig` file found in your home directory.  

```
[diff]
    tool = default-difftool
[difftool "default-difftool"]
    cmd = code --wait --diff $LOCAL $REMOTE
```
