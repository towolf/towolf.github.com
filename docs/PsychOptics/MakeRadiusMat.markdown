---
layout: mfile
title: MakeRadiusMat
categories:
  - PsychOptics
encoding: UTF-8
---

radius = MakeRadiusMat(nx,ny,centerx,[centery])

Return an n by n matrix whose entries are the
radial distance in pixels from the center pixel.

This matrix is a useful thing to pre-compute for
performing certain 2D image processing operations.

The no-loop algorithm is due to Stan Klein.

7/11/94     dhb     Slick version.