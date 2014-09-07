---
layout: mfile
title: AlphaSourceTerm
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

newSourceMat=AlphaSourceTerm(sourceFactorStr, sourceMat, destinationMat)

AlphaSourceTerm simuluates the step of multplying an alpha factor with the
source image in OpenGL alpha blending.

Apply an OpenGL source factor rule such as 'GL\_ZERO' to the image matrix
'sourceMat', returing the dot product of sourceMat and the alpha factor
selected by string 'sourceFactorStr'.

The destination image matrix 'destinationMat' is required because source
factor strings may select alpha values from the destination.

AlphaSourceTerm calculates with double-precision (64-bit) floating point
arithmatitic whereas the precision of an OpenGL renderer which it
simulates is unspecified, except that OpenGL guarantees perfect precision
for alpha values 0 and 1 (255 via [Screen](/docs/Screen)).  Comparison of AlphaSourceTerm
with the OpenGL renderer shows that alpha multiplicaion discards up to
one bit of precision.

see also: AlphaDestinationProduct PsychAlphaBlending


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychAlphaBlending/AlphaSourceTerm.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychAlphaBlending/AlphaSourceTerm.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychAlphaBlending/AlphaSourceTerm.m</code>
</div>
