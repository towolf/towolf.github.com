---
layout: mfile
title: ComputeGammaPow
categories:
  - PsychGamma
encoding: UTF-8
---

output = ComputeGammaPow(x,input)

Compute the gamma table using simple gamma function.

Largest value in input must be the maximum device
setting.  This is wise during measurements in
any case.

output = ((input/maxInput).^x(1));

10/3/93  dhb,jms  Normalize output to max of 1, remove old x(1).
                  Better be sure that last value is max setting.
8/7/00   dhb      Modify convention with gamma to be consistent
                  with extended gamma function.
                  Get rid of explicity normalization.