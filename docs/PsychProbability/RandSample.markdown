---
layout: mfile
title: RandSample
categories:
  - PsychProbability
encoding: UTF-8
---

x=RandSample(list,[dims])

Returns a random sample from a list. The optional second argument may be
used to request an array (of size dims) of independent samples. E.g.
RandSample(-1:1,[10,10]) returns a 10x10 array of samples from the list
-1:1.  RandSample is a quick way to generate samples (e.g. visual noise)
from a bounded Gaussian distribution. Also see RAND, RANDN, [Randi](/docs/Randi),
RandSel, [Sample](/docs/Sample), and [Shuffle](/docs/Shuffle).

"list" can be a double, char, cell, or struct array, but it must be a
vector (1xn or nx1). In the future, we may accept matrices (mxn) and treat
columns separately, as other Matlab functions do.