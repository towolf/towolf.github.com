---
layout: mfile
title: PlayMoviesWithoutGapDemo1
categories:
  - MovieDemos
encoding: UTF-8
---


PlayMoviesWithoutGapDemo1(moviename)

This demo accepts a pattern for a valid moviename, e.g.,
moviename='\*.mpg', then it plays all movies in the current working
directory whose names match the provided pattern, e.g., the '\*.mpg'
pattern would play all MPEG files in the current directory.

Pressing ESC ends the demo.

Movies are played one after each other. We try to minimize perceptible
gaps between end of movie i and start of movie i+1 by asynchronous
loading: While movie i is played back, we ask Psychtoolbox to load the
next movie i+1 in the background, so startup time for movie i+1 will be
minimized.