---
layout: mfile
title: ComputeWeibYN
categories:
  - Psychometric
encoding: UTF-8
---

pyes = ComputeWeibYN(x,alpha,beta)

Compute the value of a yes-no weibull psychometric function.
If 'x' is a matrix and the parameters are scalars, the same
psychometric function is applied to the whole matrix.
If 'x' is a matrix and the parameters are vectors, the
parameters are taken as applying to separate columns.

   pyes = ( 1.0 - exp( - (x./alpha).^beta ) )

9/15/93  jms  Added some special casing to deal with matrix inputs
              with/without vectors of parameters