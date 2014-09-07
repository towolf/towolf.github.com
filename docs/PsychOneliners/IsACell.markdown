---
layout: mfile
title: IsACell
categories:
  - PsychOneliners
encoding: UTF-8
---

bool = IsACell(input,fhndl)

checks if there is any element in the cell INPUT that satisfies the
logical condition in function FHNDL
works recursively: cells in cells (etc) also checked
the function FHNDL must return a scalar

examples:
checks if there is any struct in the cell:
fhndl = @isstruct
check if there is any element in the cell extending
over more than 2 dimensions:
fhndl = @(x)ndims(x)\>2

DN    2008-05-28