---
layout: mfile
title: BitsPlusPackColorImage
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

[outImage,inImage] = BitsPlusPackColorImage(inImage,[SPACESCALE],[COLORSCALE]))

Convert an image for Bits++, assuming it will
displayed on an even pixel boundary and that
it has an even number of columns.

Image is resized if SPACESCALE == 1 (default).
Otherwise scaling is assumed to have been done in advance.

Assume input is in range 0-1 if COLORSCALE == 1 (default).
Assume input is in range 0-65535 and be integer if COLORSCALE == 0.

If scaling in space, must scale in color, otherwise interpolation
can violate assumptions of prescaled color (e.g. integer vals).

8/9/04  dhb     Wrote it.
18/4/05   ejw     Converted it to run with OSX version of Psychtoolbox.
26\.2.07   mk      Bugfix for LSB conversion: Added modulo operation.
3/01/07   mk      Bugfix for MSB conversion: Added floor operation.