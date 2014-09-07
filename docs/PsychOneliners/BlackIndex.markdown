---
layout: mfile
title: BlackIndex
categories:
  - PsychOneliners
encoding: UTF-8
---

color=BlackIndex(windowPtrOrScreenNumber)
Returns the CLUT index to produce black at the current screen depth,
assuming a standard color lookup table for that depth. E.g.
black=BlackIndex(w);
[Screen](/docs/Screen)(w,'FillRect',black);

See WhiteIndex.

When the screen is 1 to 8 bit mode, the Macintosh OS always makes the
first clut element white and the last black. In 16 or 32 bit mode the
clut goes from black to white. These CLUT conventions can be overridden
by [Screen](/docs/Screen) 'SetClut', which makes a direct call to the video driver,
bypassing the Mac OS, allowing you to impose any CLUT whatsoever.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/BlackIndex.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/BlackIndex.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/BlackIndex.m</code>
</div>
