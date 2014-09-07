---
layout: mfile
title: CombVec
categories:
  - PsychProbability
encoding: UTF-8
---

CombVec Generate all possible combinations of input vectors.

   CombVec(A1,A2,...) takes any number of inputs,
      A1 - Matrix of N1 (column) vectors.
      A2 - Matrix of N2 (column) vectors.
      ...
    and returns a matrix of (N1\*N2\*...) column vectors, where the columns
    consist of all possibilities of A2 vectors, appended to
    A1 vectors, etc.

  Example

    a1 = [1 2];
    a2 = [3 4; 3 4];
    a3 = CombVec(a1,a2)
    a3 =
        1     2     1     2
        3     3     4     4
        3     3     4     4