---
layout: mfile
title: OffsetRect
categories:
  - PsychRects
encoding: UTF-8
---

newRect = OffsetRect(oldRect,x,y)

Offset the passed rect matrix by the horizontal (x)
and vertical (y) shift given. You can also pass in column vectors x and y
with e.g., n different "shifts" and the function will return n copies of
oldRect, each shifted by one of the shift values in x and y.

Alternatively you can give a single scalar x,y shift value, but apply it
to a whole matrix of rects 'oldRect' --\> Apply a common offset to a large
number of rects simultaneously.

Also see PsychRects.