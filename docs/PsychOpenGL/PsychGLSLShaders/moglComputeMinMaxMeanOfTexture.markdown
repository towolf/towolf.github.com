---
layout: mfile
title: moglComputeMinMaxMeanOfTexture
categories:
  - PsychGLSLShaders
encoding: UTF-8
---

[minv, maxv, meanv] = moglComputeMinMaxMeanOfTexture(texid, pingpongfbo1, pingpongfbo2, fastpath)

This function expects a square RGB texture as input, whose color channels
contain identical values L=R=G=B where L is a grayscale (luminance) input
image. It computes and returns its global minimum, maximum and mean luminance
on the GPU.

The width and height of the texture need to be divisible by two (even numbers).
It only works on RECTANGLE textures, not on standard power-of-two textures!
You are not allowed to use an input texture 'texid' that is identical to
the color buffer texture of the FBO 'pingpongfbo2'!