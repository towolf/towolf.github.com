---
layout: mfile
title: glmSetSwapInterval
categories:
  - wrap
encoding: UTF-8
---

glmSetSwapInterval  Set number of video frames between buffer flushes

usage:  glmSetSwapInterval\( nframes \)

Note:  The AGL documentation indicates that 'nframes' will control the
number of vertical refreshes between buffer flushes.  In practice, it seems
that nframes=0 disables vertical refresh syncing, and nframes=1 or higher
just enables it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/glmSetSwapInterval.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/glmSetSwapInterval.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/glmSetSwapInterval.m</code>
</div>
