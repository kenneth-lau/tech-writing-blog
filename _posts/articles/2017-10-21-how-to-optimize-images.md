---
layout: post
title: "How to optimize images"
excerpt: "Optimize images"
categories: articles
tags: [docs]
comments: true
share: true
modified: 2017-10-21
---

<!-- Draft -->

This explains how to optimize images using [pngquant](https://pngquant.org/). More info at https://pngquant.org/.

## What it does
Reduces the file size of PNG images. 

## Why?
Based on a Google article about image optimization: [Image Optimization](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization#tools_and_parameter_tuning)

## What to do
Note: This is for Mac users with Homebrew installed.

1. Run the following commands in the terminal

```shell
# Install pngquant using Homebrew
$ brew install pngquant
  
# Go to the directory with your images
$ cd path/to/your/images
  
# Convert all PNG files in the directory
$ pngquant 256 *.png
```

