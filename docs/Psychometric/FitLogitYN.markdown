---
layout: mfile
title: FitLogitYN
categories:
  - Psychometric
encoding: UTF-8
---

[a,b,thresh50] = FitLogistic(inputs,nYes,nNo)

Fit a logistic function to YN psychometric data.
Returns logistic parameters and 50% threshold.

The form of the logistic equation is pYes = 1/(1+10^-(a\*inputs+b))

The logistic is not a good function to use for serious work,
but you can do a quick and dirty fit analytically and
you can explain it to students more easily than some
other candidate models for psychometric functions.

See also: FitLogistic, FitWeibYN, FitCumNormYN,
 InvertLogistic, ComputeLogistic.

2/8/97      dhb     Wrote it.