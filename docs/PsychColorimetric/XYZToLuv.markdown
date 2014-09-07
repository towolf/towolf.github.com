---
layout: mfile
title: XYZToLuv
categories:
  - PsychColorimetric
encoding: UTF-8
---

luv = XYZToLuv(xyz,whiteXYZ)

xyz is a 3 x N matrix with xyz in columns
whiteXYZ is a 3 vector of the white point
luv is a 3 x N matrix with L\*u\*v\* in the columns

Formulae are taken from Wyszecki and Stiles, page 167.

xx/xx/xx    baw  Created.
xx/xx/xx    dhb  Made compatible with version 3.5
10/10/93    dhb  Changed name to XYZToLuv
5/9/02      dhb  Improved help.