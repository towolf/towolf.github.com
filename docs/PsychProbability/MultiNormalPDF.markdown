---
layout: mfile
title: MultiNormalPDF
categories:
  - PsychProbability
encoding: UTF-8
---

prob = NormalPDF(x,u,K)

Computes the p(x) according to N(u,K). Vectors x and u should be column
vectors.

Formula taken from Duda and Hart, page 23.

Does not work properly if K is singular. Does not check for dimensional
correctness.