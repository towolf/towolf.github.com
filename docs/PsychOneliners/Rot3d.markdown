---
layout: mfile
title: Rot3d
categories:
  - PsychOneliners
encoding: UTF-8
---

out = Rot3d(in,n,dim)
rotates input matrix around x-, y- of z-axis
IN is a vector, a 2D or a 3D matrix (all three can be rotated three
dimensionally)

rotation can only be performed by multiples of 90 degrees, N is the
number of 90 degree steps by which the matrix will be rotated (clockwise,
same as rot90())
DIM indicates the axis to rotate about:
  1=y; 2=x; 3=z

Rot3d([1 2 3 4; 3 5 6 7],1,1)
  ans(:,:,1) =
       4
       7
  ans(:,:,2) =
       3
       6
  ans(:,:,3) =
       2
       5
  ans(:,:,4) =
       1
       3