---
layout: mfile
title: MakeSincImage
categories:
  - PsychOneliners
encoding: UTF-8
---

image =  MakeSincImage(freq,i0,j0,nRowPixels,[nColPixels])

Computes a two-dimensional sinc function image.
The sinc function has cut-off frequency freq
(in cycles/image) and is positioned at (i0,j0).

The image has dimensions nRowPixels by nColPixels.
If nColPixels is omitted, a square image is returned.

8/15/94     dhb     Added optional column pixels argument.
10/28/98    dhb     Change to call Matlab sinc rather than my Sinc.