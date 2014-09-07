---
layout: mfile
title: ComputeWeibTAFC
categories:
  - Psychometric
encoding: UTF-8
---

pCorrect = ComputeWeibTAFC(x,alpha,beta)

Compute the value of a TAFC weibull psychometric function.
If 'x' is a matrix and the parameters are scalars, the same
psychometric function is applied to the whole matrix.
If 'x' is a matrix and the parameters are vectors, the
parameters are taken as applying to separate columns.

   pCorrect = ( 1.0 - 0.5\*exp( - (x./alpha).^beta ) )

9/15/93  jms         Added some special casing to deal with matrix inputs
                     with/without vectors of parameters
8/26/94  dhb, ccc      Handle weird values of alpha, beta
10/13/00 dhb         Improve initial guess for alpha.  Thanks to Duje Tadin
                     for identifying the need for this.