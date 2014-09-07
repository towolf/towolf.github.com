---
layout: mfile
title: NormalCumulative
categories:
  - PsychProbability
encoding: UTF-8
---

function prob = NormalCumulative(x,u,var)

Compute the probability that a draw from a N(u,var) distribution is less
than x.

6/25/96  dhb  Fixed for new erf convention.
7/24/04  awi  Cosmetic