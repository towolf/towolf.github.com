---
layout: mfile
title: kPsychNeed16BPCFloat
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

rval = kPsychNeed16BPCFloat

Return a flag that you can pass to the 'imagingmode' parameter of
[Screen](/docs/Screen)('OpenWindow') in order to request support for internal
framebuffers that store color information with 16 bits per color
component in floating point format.

If requested and supported by the graphics hardware, Psychtoolbox will
configure itself to store and process all color information as 16 bit
floating point numbers, so called OpenGL half\_floats.

FIXME: More info...

It is part of the Psychtoolbox imaging pipeline and only works on modern
graphics hardware, e.g., ATI Radeon 9600 and later, NVidia GeforceFX 5000
and later. Check the www.psychtoolbox.org Wiki for graphics hardware
recommendations and for a description of PTB's image processing
capabilities.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/kPsychNeed16BPCFloat.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/kPsychNeed16BPCFloat.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/kPsychNeed16BPCFloat.m</code>
</div>
