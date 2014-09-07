---
layout: mfile
title: ImageToCalFormat
categories:
  - PsychCal
encoding: UTF-8
---

[calFormat,nX,nY] = ImageToCalFormat(image)

Take an nX (col dimension) by nY (row dimension) by k image
and convert it to a format that may be used to Psychtoolbox
calibration routines.

Note that the order nX,nY makes sense for thinking about images
in terms of x and y coordinates, but that the order is backwards
from the MATLAB convention of row dim then column dim.

See also CalFormatToImage

8/04/04  dhb  Wrote it.
7/16/07  dhb  Update help line.
10/2/09  dhb  Try again on making help clear.