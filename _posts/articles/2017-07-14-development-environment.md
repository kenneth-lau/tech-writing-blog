---
layout: post
title: "My working environment"
excerpt: "Examples and code for displaying images in posts."
categories: articles
tags: [sample-post, images, test]
comments: true
share: true
modified: 2017-07-17
---

Setting up a new computer. 

Here's what you need to do.

## Install Xcode Command Line Tools


1. Check whether you have Xcode installed

        ```
        $ xcode-select -p
        ```

2. Install Xcode Command Line Tools

        ```
        $ xcode-select --install
        ```

## Configure git

## Install Homebrew

## Install Ruby

### GPG

### RVM

1. Install RVM

```shell
$ \curl -L https://get.rvm.io | bash -s stable
```

2. Restart the terminal

```shell
source ~/.rvm/scripts/rvm
```

3. Test RVM configuration

```
shell
type rvm | head -n 1
```

### Install Ruby

1. 
```shell
$ rvm install ruby-2.4.1
```

2. Verify the version of Ruby

```shell
$ ruby -v
```

### RubyGems


1. Show gems that need to be updated

```shell
$ gem outdated
```

1. Update gems

```shell
$ gem update
```

2. Install Bundler

```shell
$ gem install bundler
```

3. Install Nokogiri

```shell
$ gem install nokogiri
```

## Reference

[Installing Ruby on Rails for Mac](http://railsapps.github.io/installrubyonrails-mac.html)


## Jekyll

1. Install Jekyll

```shell
$ gem install jekyll
```

2. Update Jekyll

```shell
$ gem update jekyll
```

