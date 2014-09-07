---
layout: mfile
title: PR705measspd
categories:
  - PR705Toolbox
---

PR705measspd \- Get a spectral power distribution from the PR\-705.

Syntax:
spd = PR705measspd\(\[S\]\)

Input:
S \(1x3\) \- Desired wavelength sampling. Default: \[380 5 81\]

Output:
spd \(Nx1\) \- The spectral power distribution \(N = S\(3\) or 81 by default\).

12/06/12   zlb   Wrote it loosely based on the PR670Toolbox.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/PR705Toolbox/PR705measspd.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/PR705Toolbox/PR705measspd.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/PR705Toolbox/PR705measspd.m</code>
</div>
