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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/XYZToLuv.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/XYZToLuv.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/XYZToLuv.m</code>
</div>
