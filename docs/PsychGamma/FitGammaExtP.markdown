---
layout: mfile
title: FitGammaExtP
categories:
  - PsychGamma
encoding: UTF-8
---

[fit\_out,x,err] = FitGammaPow(values\_in,measurements,values\_out,x0)

Fit extended power function to gamma data.

4/08/02 awi Turned off warnings before calling constr to avoid future obsolete warning.
4/13/02 dgp Fixed the warning suppression to save and restore original state.
3/4/05  dhb   Handle new version of optimization toolbox.