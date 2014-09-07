---
layout: mfile
title: MunsellHueToAngle
categories:
  - PsychMunsell
encoding: UTF-8
---

angle = MunsellHueToAngle(H1,H2)

Convert a standard Munsell hue designation to an angle

The hue designation consists of a leading number
(e.g. 2.5, 5, 7.5, 10) and a symbolic hue name.

We convert these to angle using the convention specified
on page 509 of Wyszecki and Stiles, 2cd edition.  Angle
is in degrees increasing counterclockwise form the positive
x-axis in the diagram.

See also: MunsellAngleToHue

dhb, ijk  Wrote it.