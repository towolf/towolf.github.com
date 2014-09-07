---
layout: mfile
title: PlayDualMoviesDemo
categories:
  - MovieDemos
encoding: UTF-8
---


PlayDualMoviesDemo(moviename)

This demo accepts a pattern for a valid moviename, e.g.,
moviename='\*.mpg', then it plays all movies in the current working
directory whose names match the provided pattern, e.g., the '\*.mpg'
pattern would play all MPEG files in the current directory.

This demo uses automatic asynchronous playback for synchronized playback
of video and sound. Each movie plays until end, then rewinds and plays
again from the start. Pressing the Cursor-Up/Down key pauses/unpauses the
movie and increases/decreases playback rate.
The left- right arrow keys jump in 1 seconds steps. SPACE jumps to the
next movie in the list. ESC ends the demo.
