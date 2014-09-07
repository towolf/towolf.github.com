---
layout: mfile
title: ShrinkMatrix
categories:
  - PsychOneliners
encoding: UTF-8
---

out = ShrinkMatrix(IN, FAC)
Shrinks a 2-D or 3-D matrix IN (an image) by a factor FAC.
matrix will be truncated horizontally and vertically so that the
resultant shrunk matrix would have integer sizes in the x an y dimension.
size of 3rd dimension will not be scaled.
shrinking is performed by mean computation.