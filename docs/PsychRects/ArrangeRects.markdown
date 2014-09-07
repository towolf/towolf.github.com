---
layout: mfile
title: ArrangeRects
categories:
  - PsychRects
encoding: UTF-8
---

cellRects=ArrangeRects(n,objectRect,windowRect,[rightToLeft]);

Returns an array of n contiguous rects that achieve a visually
pleasing arrangement of n objects of size objectRect within a
window of size windowRect. Each row of the returned matrix is a rect.
If the rightToLeft argument is supplied and nonzero then
the cells are ordered right to left (like Hebrew letters).
Otherwise they are ordered left to right (like English letters).
The result depends on the proportions of the objectRect, but is
independent of its size and position.
Also see PsychRects.