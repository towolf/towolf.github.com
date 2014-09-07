---
layout: mfile
title: ComputeGammaSig
categories:
  - PsychGamma
encoding: UTF-8
---

output = ComputeGammaSig(x,input)

Compute the gamma table using sigmoidal function.

sinput = (input/x(3)).^x(4);
output = x(2).\*sinput./(sinput + x(1));

10/3/93  dhb,jms  Normalize output to max of 1.
                  Better be sure that last value is max setting.