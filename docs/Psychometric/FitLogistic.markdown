---
layout: mfile
title: FitLogistic
categories:
  - Psychometric
encoding: UTF-8
---

[a,b] = FitLogistic(x,y)

Fit a logistic function to the data pairs x,y.

The form of the logistic equation is y = 1/(1+10^-(ax+b)).
The method used here is to regres on transformed coordinates.
One could use search to do a maximum likelihood function for
psychometric data, but if you are going to do that, you
should probably fit a cumulative normal or Weibull function.

See also: ComputeLogistic, InvertLogistic, FitLogitYN, FitWeibTAFC,
  FitWeibYN, FitAlphaWeibTAFC.

2/15/95     dhb     Wrote it.