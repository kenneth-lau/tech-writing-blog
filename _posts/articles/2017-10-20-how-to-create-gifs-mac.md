---
layout: post
title: "How to create GIFs on a Mac"
excerpt: "Create GIFs"
categories: articles
tags: [docs]
comments: true
share: true
modified: 2017-10-20
---

<!-- Draft -->

This describes how to create GIF files of a screen recording using [FFmpeg](https://www.ffmpeg.org/).

## Install FFmpeg using Homebrew

1. Run the following to install FFmpeg (Note: You must have Homebrew installed.)

```shell
$ brew install ffmpeg
```

2. Check that FFmpeg is installed

```shell
$ brew list
```

## Create a recording of the device

1. Connect device to your computer
1. Open Quicktime
1. Under "File", select "New Movie Recording"
1. Select your external device from the drop-down menu
1. Create your recording
1. Save the recording

## Convert the .mov file to a .png file

Run the following command

```shell
ffmpeg -i ios-sdk-starter.mov -i ios-sdk-starter.png -lavfi fps=20,paletteuse -y ios-sdk-starter.gif
```

## Example

ffmpeg -i just-java.mov -lavfi fps=20,paletteuse -y just-java.gif

ffmpeg -i just-java.mov -pix_fmt just-java.gif

ffmpeg -i just-java.mov just-java.png 

ffmpeg -y -i just-java.mov \
-vf fps=10,scale=320:-1:flags=lanczos,palettegen just-java.png

ffmpeg -i just-java.mov -r 10 just-java.png 