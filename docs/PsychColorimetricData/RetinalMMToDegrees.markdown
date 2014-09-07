---
layout: mfile
title: RetinalMMToDegrees
categories:
  - PsychColorimetricData
encoding: UTF-8
---

degs = RetinalMMToDegrees(mm,eyeLengthMM)

Convert extent in mm of retina in the fovea to degrees
of visual angle.

This is implemented as the simple trigonometric formula,
and is most valid for small angles around the fovea.

See also: DegreesToRetinalMM, EyeLength.

7/15/03  dhb  Wrote it.