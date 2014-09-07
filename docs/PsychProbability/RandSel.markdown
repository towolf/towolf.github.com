---
layout: mfile
title: RandSel
categories:
  - PsychProbability
encoding: UTF-8
---

sel = RandSel(in,n)
  if N is a scalar
    randomly selects N elements from set IN, elements are replenished.
    Output is of size 1xN
  if N is a vector
    randomly selects prod(N) elements from set IN, with replenishment. N
    specifies the shape of the output, e.g., if N=[10 10 5], SEL will be
    a 10x10x5 matrix
  IN can be of any datatype and can have any number of dimensions and
  elements