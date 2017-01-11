---
Title: Ffmpeg webm video encoding, seeking and scaling
Date: 2017-01-10 11:27
Category: media
Tags: ffmpeg
Authors: sedlav
---

## Webm video encoding,

libvpx is the VP8 video encoder for ​WebM, an open, royalty-free media file format. This guide is an attempt to summarize the most important options for creating video with libvpx. To install FFmpeg with support for libvpx, look at the Compilation Guides and compile FFmpeg with the --enable-libvpx option.

[Link](https://trac.ffmpeg.org/wiki/Encode/VP8)

## seeking

If you need to extract only a specific part of your input, you'll need to use the seeking option to get to that specific part in the input first. ​The parameter -ss is used to seek within the input and it can be used in several ways.

[Link](https://trac.ffmpeg.org/wiki/Seeking)

## Scaling

FFmpeg has got a very powerful scale filter, which can be used to accomplish various tasks ... If you need to simply resize your video to a specific size (e.g 320x240), you can use the scale filter in its most basic form...

[Link](https://trac.ffmpeg.org/wiki/Scaling%20(resizing)%20with%20ffmpeg)
