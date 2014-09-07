---
layout: mfile
title: MonoImageToSRGB
categories:
  - PsychColorimetric
encoding: UTF-8
---

rgbImage = MonoImageToSRGB(monoImage,xy,[SCALE])

Take a single plane image in and convert to an sRGB standard
color image out.  The chromaticity of the output image will
be at the specify CIE x,y chromaticity value.

Result is a uint8 image scaled into range [0,255].

The value of SCALE is passed on to SRGBGammaCorrect, and
there determines whether autoscaling is applied to the image.

See MonoImageToSRGBTest.

6/15/11  dhb, ms  Wrote it.