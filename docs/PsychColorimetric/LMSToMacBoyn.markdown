---
layout: mfile
title: LMSToMacBoyn
categories:
  - PsychColorimetric
encoding: UTF-8
---

ls = LMSToMacBoyn(LMS,[T\_cones,T\_lum])

Compute MacLeod-Boynton chromaticity from
cone coordinates.

If T\_cones and T\_lum are not passed, we assume
Smith-Pokorny sensitivities normalized to a
peak of 1.  I T\_cones and T\_lum are passed,
we compute the scalings of the L and M cones
required to best predict lumiance and scale
accordingly.

10/30/97  dhb  Wrote it.
7/9/02    dhb  T\_cones\_sp -\> T\_cones on line 20.  Thanks to Eiji Kimura.