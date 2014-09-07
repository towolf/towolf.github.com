---
layout: mfile
title: PlayInterlacedMovieDemo
categories:
  - MovieDemos
encoding: UTF-8
---


PlayInterlacedMovieDemo(moviename)

A simple demo to show playback of interlaced movies. Input
images from the movie are deinterlaced on-the-fly by use of a simple GLSL
deinterlace shader.

The demo reads a movie file from the file 'moviename' and plays it once,
then exits.

Should work with NVidia GeforceFX 5200 or ATI Radeon 9600 and later, or
Intel GMA 950.