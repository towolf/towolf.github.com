---
layout: mfile
title: UniqueNoSorting
categories:
  - PsychProbability
encoding: UTF-8
---

output = UniqueNoSorting(sequence,mode)

SEQUENCE is a vector, MODE is a specification of how you want your output
to be not sorted.

Basically the same as unique, but returns the unique values either:
"in order of appearance"        - (MODE = 'first' for 'first occurrence')
or
"in order of disappearance"     - (MODE = 'last'  for 'last occurrence')

MODE defaults to 'first'

JvR 2008-05-06