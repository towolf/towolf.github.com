---
layout: mfile
title: FitGammaWeib
categories:
  - PsychGamma
encoding: UTF-8
---

[fit\_out,x,err] = FitGammaWeib(values\_in,measurements,values\_out,x0)

Fits a Weibull function to the passed gamma data.

10/3/93   dhb   Created from jms code to fit psychometric functions
3/4/05      dhb   Conditionals for optimization toolbox version.
                    dhb     Encapsulate error calculation