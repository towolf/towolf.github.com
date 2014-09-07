---
layout: mfile
title: ComputeFSSE
categories:
  - PsychGamma
encoding: UTF-8
---

rmse = ComputeFSSE(data,predict)  

Compute a root fractional SSE between data and prediction.  
Inputs should be column vectors.  
Actual code is:  
  diff = predict-data;  
  rmse = sqrt((diff'\*diff)/(data'\*data));  

7/9/14  dhb  Wrote this.  Will replace calls to old and badly named ComputeRMSE  
             with calls to this.  This does what ComputeRMSE did, but the  
             bad name of ComputeRMSE was bugging me too much.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGamma/ComputeFSSE.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGamma/ComputeFSSE.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGamma/ComputeFSSE.m</code>
</div>
