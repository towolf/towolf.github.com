---
layout: mfile
title: ComputeGammaPoly
categories:
  - PsychGamma
encoding: UTF-8
---

output = ComputeGammaPoly(x,input)

Compute gamma table using polynomial function.
Relies on Matlab's built-in polyeval.

Assumes that 1 is maximum input value

10/3/93  dhb,jms  Normalize output to max of 1.
                  Better be sure that last value is max setting.
10/4/93  dhb      Force monotonicity
6/5/10   dhb      Update for [0,1] input convention.