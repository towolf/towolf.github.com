---
layout: mfile
title: Expand
categories:
  - PsychSignal
---

B=[Expand](/docs/Expand)\(A,horizontalFactor,\[verticalFactor\]\)

Expands the ND matrix A by cell replication, and returns the result.
If the vertical scale factor is omitted, it is assumed to be
the same as the horizontal. Note that the horizontal\-before\-vertical
ordering of arguments is consistent with image processing, but contrary
to Matlab's rows\-before\-columns convention.

We use "Tony's Trick" to replicate a vector, as explained
in MathWorks Matlab Technote 1109, section 4.

Also see ScaleRect.m


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychSignal/Expand.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychSignal/Expand.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychSignal/Expand.m</code>
</div>
