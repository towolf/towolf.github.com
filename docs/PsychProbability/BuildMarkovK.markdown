---
layout: mfile
title: BuildMarkovK
categories:
  - PsychProbability
encoding: UTF-8
---

K = BuildMarkovK(n,r,var)
K = BuildMarkovK(r,var)

Build the covariance matrix for a Markov process as defined in Pratt, pp.
131 ff.

This routine has two calling forms.  In the first form, three arguments
are passed and the random variables are assumed to have the save
variance.  Thus the passed var is a scalar.

In the second form, the passed var is a column vector containing the
variances of the individual random variables.

8/19/94     dhb     Wrote it.
2/6/96      dhb     Second calling form.
7/24/04       awi     Cosmetic.