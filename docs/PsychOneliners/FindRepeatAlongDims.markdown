---
layout: mfile
title: FindRepeatAlongDims
categories:
  - PsychOneliners
encoding: UTF-8
---

find repeated rows or columns in a matrix.
inds = FindRepeatAlongDims(in,dim)
example:
in =
     1     2     3
     2     3     4
     4     5     6
     1     2     3
     1     2     3
     4     5     6
FindRepeatAlongDims(in,1)  % check for repeated rows
ans =
     5                    % the fifth row is the same as the fourth row,
                            repeat!

for N-D dimensions, this function can also find repeats along the highest
dimension, such as finding repeated planes in a 3D matrix.