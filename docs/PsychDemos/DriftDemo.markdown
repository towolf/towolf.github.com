---
layout: mfile
title: DriftDemo
categories:
  - PsychDemos
encoding: UTF-8
---

DriftDemo
----

Display an animated grating using the new [Screen](/docs/Screen)('DrawTexture') command.
In Psychtoolbox-3 [Screen](/docs/Screen)('DrawTexture') replaces
[Screen](/docs/Screen)('CopyWindow').

This is a very simple, bare bones demo on how to do frame animation. For
much more efficient ways to draw gratings and gabors, have a look at
DriftDemo2, DriftDemo3, DriftDemo4, ProceduralGaborDemo, GarboriumDemo,
ProceduralGarboriumDemo and DriftWaitDemo.

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

see also: PsychDemos, MovieDemo


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/DriftDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/DriftDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/DriftDemo.m</code>
</div>
