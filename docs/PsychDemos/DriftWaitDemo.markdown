---
layout: mfile
title: DriftWaitDemo
categories:
  - PsychDemos
encoding: UTF-8
---

DriftWaitDemo([movieDurationSecs=10][, waitframes=1])
----

Display an animated grating using the new [Screen](/docs/Screen)('DrawTexture') command.
In Psychtoolbox-3 [Screen](/docs/Screen)('DrawTexture') replaces [Screen](/docs/Screen)('CopyWindow').

This demo illustrates on how to emulate the old [Screen](/docs/Screen)('WaitBlanking'...)
behaviour: If you set waitframes \> 1 then the screen is only updated
every waitframes'th monitor refresh interval.

# Optional parameters:

movieDurationSecs == Requested total duration of movie in seconds.
waitframes == Number of monitor refresh intervals to wait before each
frame is drawn.

# CopyWindow vs. DrawTexture:

In the OS 9 Psychtoolbox, [Screen](/docs/Screen) ('CopyWindow") was used for all
time-critical display of images, in particular for display of the movie
frames in animated stimuli. In contrast, [Screen](/docs/Screen)('DrawTexture') should not
be used for display of all graphic elements,  but only for  display of
MATLAB matrices.  For all other graphical elements, such as lines,  rectangles,
and ovals we recommend that these be drawn directly to the  display
window during the animation rather than rendered to offscreen  windows
prior to the animation.
----

see also: PsychDemos, MovieDemo, DriftDemo