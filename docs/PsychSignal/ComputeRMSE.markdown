---
layout: mfile
title: ComputeRMSE
categories:
  - PsychSignal
encoding: UTF-8
---

 rmse = ComputeRMSE\(data,predict\)

 Compute fractional RMSE between data and prediction.
 Inputs should be column vectors.
 Actual code is:
        diff = predict-data;
        rmse = sqrt\(\(diff'\*diff\)/\(data'\*data\)\);

 2/3/96     dhb     Added improved comments.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychSignal/ComputeRMSE.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychSignal/ComputeRMSE.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychSignal/ComputeRMSE.m</code>
</div>
