---
layout: mfile
title: AlphaImageDemo
categories:
  - AlphaImageDemo
---

AlphaImageDemo

Display a gaussian masked image, locked to the cursor position,
using the [Screen](/docs/Screen)\('DrawTexture'\) command.

This illustrates an application of OpenGL Alpha blending by displaying
an image masked with a gaussian transparency mask.

In each frame, first the image is drawn. Then a texture acting as a
transparency mask is drawn "over" the image, leaving only selected
parts of the image.

Please note that we only use two textures: One holding the image,
the other defining the mask.

see also: PsychDemos, MovieDemo, DriftDemo


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/AlphaImageDemo/AlphaImageDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/AlphaImageDemo/AlphaImageDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/AlphaImageDemo/AlphaImageDemo.m</code>
</div>
