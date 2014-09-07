---
layout: mfile
title: ClutAnimDemo
categories:
  - PsychDemos
encoding: UTF-8
---

ClutAnimDemo\(\[method=0\]\)

Display an animated grating using CLUT animation via the
[Screen](/docs/Screen)\('LoadNormalizedGammaTable'\) command, or via the PsychImaging\(\)
based clut animation support.

If 'method' is left out or set to 0, hardware gamma tables are
immediately updated. A setting of 1 will update hardware gamma tables in
sync with [Screen](/docs/Screen)\('[Flip](/docs/Flip)'\), or more accurately, it will try to.
Synchronization can't be guaranteed, only that a good effort is made to
achieve sync. A 'method' setting of 2 will use the Psychtoolbox image
processing pipeline to implement clut animation, instead of updating the
hardware gamma tables. This is the only reliable method with respect to
timing precision. It is also the only method that works on MS-Windows.
However, it requires recent graphics hardware and a bit more computation
time.

Method 2 is recommended for most use cases, method 0 is the least
reliable one.

see also: PsychDemos, PsychImaging



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/ClutAnimDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/ClutAnimDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/ClutAnimDemo.m</code>
</div>
