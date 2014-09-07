---
layout: mfile
title: SimpleMovieDemo
categories:
  - MovieDemos
encoding: UTF-8
---

Most simplistic demo on how to play a movie.

SimpleMovieDemo(moviename [, windowrect=[]]);

This bare-bones demo plays a single movie whose name has to be provided -
including the full filesystem path to the movie - exactly once, then
exits. This is the most minimalistic way of doing it. For a more complex
demo see PlayMoviesDemo. The remaining demos show more advanced concepts
like proper timing etc.

The demo will play our standard DualDiscs.mov movie if the 'moviename' is
omitted.
