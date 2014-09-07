---
layout: mfile
title: AlphaRotateDemo
categories:
  - PsychDemos
encoding: UTF-8
---

AlphaRotateDemo\(numFrames, ifis\)

numFrames Number of grating textures to use for the drifting grating...

ifis = Number of monitor refreshes to wait between drawing single
textures...


# OS X

Display a rotating grating using the new [Screen](/docs/Screen)\('DrawTexture'\) command.
In the OS X Psychtoolbox [Screen](/docs/Screen)\('DrawTexture'\) replaces
[Screen](/docs/Screen)\('CopyWindow'\).

This illustrates an application of Alpha blending by masking the rotating
grating with a gaussian transparency mask.

In each frame, first the grating is drawn. Then a texture acting as a
transparency mask is drawn "over" the grating, masking out selected
parts of the grating.
----

see also: PsychDemos, MovieDemo


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/AlphaRotateDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/AlphaRotateDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/AlphaRotateDemo.m</code>
</div>
