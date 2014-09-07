---
layout: mfile
title: MonoImageToSRGB
categories:
  - PsychColorimetric
---

rgbImage = MonoImageToSRGB\(monoImage,xy,\[SCALE\]\)

Take a single plane image in and convert to an sRGB standard
color image out.  The chromaticity of the output image will
be at the specify CIE x,y chromaticity value.

Result is a uint8 image scaled into range \[0,255\].

The value of SCALE is passed on to SRGBGammaCorrect, and
there determines whether autoscaling is applied to the image.

See MonoImageToSRGBTest.

6/15/11  dhb, ms  Wrote it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/MonoImageToSRGB.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/MonoImageToSRGB.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/MonoImageToSRGB.m</code>
</div>
