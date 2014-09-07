---
layout: mfile
title: PsychNumel
categories:
  - PsychOneliners
encoding: UTF-8
---

PTB-Replacement for numel\(\) on older Matlab versions that don't support it.

PsychNumel is a drop-in replacement for the numel\(\) function of recent
versions of Matlab. If called on modern Matlabs, it will just call
numel\(\). On older Matlabs it will emulate the behaviour of numel\(\).

n = PsychNumel\(x\); will return the total number of elements contained in
scalar, vector or matrix x, i.e. n == prod\(size\(x\)\);



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/PsychNumel.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/PsychNumel.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/PsychNumel.m</code>
</div>
