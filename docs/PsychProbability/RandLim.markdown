---
layout: mfile
title: RandLim
categories:
  - PsychProbability
encoding: UTF-8
---

returns pseudo-random values drawn from a uniform distribution with lower
and upper limits LOWER and UPPER.
LOWER and UPPER can also be matrices of the same shape as rand(N) would
create

N is a vector indicating the dimensions of the output:
  N = [3]      creates a    3x3 matrix
  N = [1,3]    creates a    1x3 matrix
  N = [17,1,3] creates a 17x1x3 matrix

LOWER and UPPER can be any number