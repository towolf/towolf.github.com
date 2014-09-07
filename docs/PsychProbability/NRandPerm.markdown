---
layout: mfile
title: NRandPerm
categories:
  - PsychProbability
encoding: UTF-8
---

NRandPerm Random permutation.
   NRandPerm(n,nret) is a random permutation of the integers from 1 to n,
   of which nret elements are returned.
   NRandPerm thus returns a random selection of integers from 1 to n with
   no repeats.

   For example, NRandPerm(6,4) might be [2 4 5 6].

   Note that NRandPerm calls RAND and therefore changes RAND's state.

   See also PERMUTE, RANDPERM.