---
layout: mfile
title: NormalROC
categories:
  - Psychometric
encoding: UTF-8
---

ROC = NormalROC(logbetas,us,vars,un,varn)

Compute ROC curve given the parameters.  Done
analytically for speed.

The trick here is to solve for the values of x
such that log(l(x)) \> logbetas.  When the variances
are unequal, there can be two distinct regions.
I basically handle this by brute force, since there
are not too many distinct cases.

This routine is not carefully tested and may
contain errors.

xx/xx/xx  dhb  Wrote it.
10/4/00   dhb  Added caveat about bug possibilities, based
               in part on disagreement between this routine
               and some Monte Carlo simulations.