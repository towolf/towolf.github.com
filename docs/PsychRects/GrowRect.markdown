---
layout: mfile
title: GrowRect
categories:
  - PsychRects
encoding: UTF-8
---

r = GrowRect(r,horizontalPixels,verticalPixels)

Grows a rect, by subtracting horizontalPixels from the left coordinate
and verticalPixels from the top coordinate, and adding horizontalPixels
to the right coordinate and verticalPixels to the bottom coordinate. Also
see ScaleRect. Input can be multiple rects, concatenated into a Mx4
matrix Using a negate number os pixels to grow by would obviously shrink
the rect, though be careful as no checks are performed to see if the
resulting rect is valid.

Also see PsychRects.