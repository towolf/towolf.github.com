---
layout: mfile
title: MakeSineImage
categories:
  - PsychOneliners
encoding: UTF-8
---

 [image] = MakeSineImage(freqi,freqj,nRowPixels,[nColPixels])

 Computes a two-dimensional sine function image.

 The image has dimensions nRowPixels by nColPixels.
 If nColPixels is omitted, a square image is returned.

 8/15/94        dhb     Both row and column dimensions used if passed.
                dhb     Changed zero frequency convention.
 6/20/98       dhb, mw Fixed error in zero handling case.