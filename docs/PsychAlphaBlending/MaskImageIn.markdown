---
layout: mfile
title: MaskImageIn
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

mMasked=MaskImageIn\(m \[,alphaIn\]\)

Accept an image matrix "m" and return "nMasked", holding the same image
but with adjusted alpha values.  MaskImageIn sets full transparency
for pixels with value zero and sets full opacity for pixels with
non-zero value.

If the optional alphaIn argument is specified then MaskImageIn sets
non-zero pixels to alphaIn opacity instad of to full opacity, 255.

see also: SetImageAlpha, MaskImageOut, AlphaDemo.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychAlphaBlending/MaskImageIn.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychAlphaBlending/MaskImageIn.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychAlphaBlending/MaskImageIn.m</code>
</div>
