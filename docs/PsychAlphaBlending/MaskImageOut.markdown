---
layout: mfile
title: MaskImageOut
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

mMasked=MaskImageOut(m [,alphaIn])

Accept an image matrix "m" and return "nMasked", holding the same image
but with adjusted alpha values.  MaskImageOut sets full opacity
for pixels with value zero and sets full transparency for pixels with
non-zero value.

If the optional alphaIn argument is specified then MaskImageIn sets
zero pixels to alphaIn opacity instad of to full opacity, 255.

see also: SetImageAlpha, MaskImageIn, AlphaDemo.