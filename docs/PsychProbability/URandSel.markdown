---
layout: mfile
title: URandSel
categories:
  - PsychProbability
encoding: UTF-8
---

sel = RandSel(in,n)
  if N is a scalar
    randomly selects N elements from set IN, each element from IN will
    be selected up to one time (so sampling without replacing).
    Output is of size 1xN
  if N is a vector
    randomly selects prod(N) elements from set IN, without replacing. N
    specifies the shape of the output, e.g., if N=[10 10 5], SEL will be
    a 10x10x5 matrix
  IN can be of any datatype and can have any number of dimensions and
  elements