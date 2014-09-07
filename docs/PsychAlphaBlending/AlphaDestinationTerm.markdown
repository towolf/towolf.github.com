---
layout: mfile
title: AlphaDestinationTerm
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

newDestinationMat=AlphaDestinationTerm(destinationFactorStr, sourceMatrix, destinationMatrix)

AlphaDestinationTerm simuluates the step of multplying an alpha factor with the
destination image in OpenGL alpha blending.

Apply an OpenGL source factor rule such as 'GL\_ZERO' to the image matrix
'destinationMat', returing the dot product of destinationMat and the
alpha factor selected by string 'sourceFactor'.

The source image matrix 'sourceMat' is required because destination
factor strings may select alpha values from the source image.

AlphaDestinationTerm calculates with double-precision (64-bit) floating
point arithmatitic whereas the precision of an OpenGL renderer which it
simulates is unspecified, except that OpenGL guarantees perfect precision
for alpha values 0 and 1 (255 via [Screen](/docs/Screen)).  Comparison of
AlphaDestinationTerm with the OpenGL renderer shows that alpha
multiplicaion discards up to one bit of precision.

see also: AlphaSourceTerm, PsychAlphaBlending