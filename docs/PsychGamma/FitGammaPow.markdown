---
layout: mfile
title: FitGammaPow
categories:
  - PsychGamma
encoding: UTF-8
---

[fit\_out,x,err] = FitGammaPow(values\_in,measurements,values\_out,x0)

Fit power function to gamma data.

NOTE: Uses Mathworks Optimization Toolbox.

Also see FitGamma, FitGammaDemo.

4/08/02 awi   Turned off warnings while calling constr to avoid future obsolete warning
3/4/05  dhb   Conditionals for optimization toolbox version.