---
layout: mfile
title: WhiteIndex
categories:
  - PsychOneliners
encoding: UTF-8
---

color=WhiteIndex(windowPtrOrScreenNumber)
Returns the intensity value to produce white at the current screen depth,
assuming a standard color lookup table for that depth. E.g.

white=WhiteIndex(w);
[Screen](/docs/Screen)(w,'FillRect',white);

windowPtrOrScreenNumber must be a screen number or a handle for
an onscreen window. It won't work on offscreen windows or textures.

See BlackIndex.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/WhiteIndex.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/WhiteIndex.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/WhiteIndex.m</code>
</div>
