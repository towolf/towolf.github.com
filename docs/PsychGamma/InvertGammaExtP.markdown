---
layout: mfile
title: InvertGammaExtP
categories:
  - PsychGamma
encoding: UTF-8
---

output = InvertGammaExpP(x,input)

Invert the gamma table using an extended power function.
See Brainard, Pelli, & Robson (2001).

Parameter x are the function parameters as returned
by FitGamma/FitGammaExtP.  See ComputeGammaExtP.

Parameter maxInput is the maximum device input
value (typically 1).

\8/7/00   dhb      Wrote it.
\6/5/10   dhb      Update for OS/X assumption of input values as real's in [0-1]


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGamma/InvertGammaExtP.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGamma/InvertGammaExtP.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGamma/InvertGammaExtP.m</code>
</div>
