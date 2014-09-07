---
layout: mfile
title: MakeGammaMonotonic
categories:
  - PsychGamma
encoding: UTF-8
---

output = MakeGammaMonotonic(input)

Make input monotonically increasing from lowest value.

This version also forces the last value to be 1, and then
enforces decreasing downwards from there, after the
enforcement of increasing from 0.

3/1/99  dhb  Handle multiple columns.
8/03/07 dhb  Old routine just enforced non-decreasing.  Fixed to make strictly increasing.
3/07/10 dhb  Wrote from MakeMonotonic.
             Did not want to change behavior of MakeMonotonic in case it is called from
             programs unrelated to gamma fitting.
3/08/10 dhb  Actually do the enforcement of 1.
5/27/10 dhb  Use a larger bump, 100\*eps