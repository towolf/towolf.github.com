---
layout: mfile
title: CenterRectOnPointd
categories:
  - PsychRects
encoding: UTF-8
---

newRect = CenterRectOnPointd(rect,x,y)

CenterRectOnPointd offsets the rect to center it around an x and y position.
The center of the rect is reported by RectCenterd. This is the same as
CenterRectOnPoint, just that it returns floating point results instead of
results that are rounded to integral pixel positions.

See also PsychRects, RectCenter, RectCenterd