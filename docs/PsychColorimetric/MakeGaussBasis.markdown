---
layout: mfile
title: MakeGaussBasis
categories:
  - PsychColorimetric
encoding: UTF-8
---

[B] = MakeGaussBasis(wls,means,vars);

Make a basis set of shifted Gaussians.  Area
under each Gaussian is unity.

1/23/96  dhb    Wrote it.
11/20/96 dhb  Make area unity, not maximum which is how it was.
12/3/99  dhb  Change documentation sds -\> vars as this is what it does.