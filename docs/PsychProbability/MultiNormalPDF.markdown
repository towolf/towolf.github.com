---
layout: mfile
title: MultiNormalPDF
categories:
  - PsychProbability
encoding: UTF-8
---

prob = NormalPDF\(x,u,K\)

Computes the p\(x\) according to N\(u,K\). Vectors x and u should be column
vectors.

Formula taken from Duda and Hart, page 23.

Does not work properly if K is singular. Does not check for dimensional
correctness.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychProbability/MultiNormalPDF.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychProbability/MultiNormalPDF.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychProbability/MultiNormalPDF.m</code>
</div>
