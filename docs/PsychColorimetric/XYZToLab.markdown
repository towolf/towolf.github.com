---
layout: mfile
title: XYZToLab
categories:
  - PsychColorimetric
encoding: UTF-8
---

lab = XYZToLab(xyz,whiteXYZ)

xyz is a 3 x N matrix with xyz in columns
whiteXYZ is a length 3 vector with the white point.
lab is a 3 x N matrix of [Lstar;astar;bstar]

Formulae are taken from Wyszecki and Stiles, page 167.

xx/xx/xx    baw  Created.
xx/xx/xx    dhb  Made compatible with version 3.5
10/10/93    dhb  Changed name to XYZToLab.
5/9/02      dhb  Improved help