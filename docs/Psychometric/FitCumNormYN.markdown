---
layout: mfile
title: FitCumNormYN
categories:
  - Psychometric
encoding: UTF-8
---

[uEst,varEst] = FitCumNormYN(inputs,nYes,nNo)

Fits a cumulative normal function to the passed yes-no data.
Requires the optimization toolbox.

# INPUTS:
  inputs:   Input levels
  nYes:     Number of yes responses at the corresponding input level
  nNo:      Number of no responses at the corresponding input level
OUTPUTS:
  uEst
  varEst

See also: FitWeibTAFC, FitFitWeibYN, FitWeibAlphTAFC, FitLogitYN

9/22/93   jms   Created from FitWeibullYN.
2/8/97    dhb   Cleaned up and added some comments.
                Check that optimization toolbox is present.
10/4/00   dhb   Fixed bugs along lines suggested by Keith Schneider.
                Case of uInitial = 0 wasn't handled properly, and
                variance search limits were set based on mean.
3/4/05      dhb   Conditionals for optimization toolbox version.