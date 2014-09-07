---
layout: mfile
title: FindThreshWeibYN
categories:
  - Psychometric
encoding: UTF-8
---

threshold = FindThreshWeibYN(pcorrect, alpha, beta)

 Invert Weibull function to find threshold
 for given pcorrect, alpha, and beta.
 This function should invert ComputeWeibullYN().

 threshold = alpha \* pow( -1.0\*log(1.0-pyes) , 1.0/beta );