---
layout: mfile
title: PR705read
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705read - Read data from the PR-705.

Syntax:
serialData = PR705read([block=0] [, nbytes])

Description:
This is a convenience wrapper to read data from the PR-705 device. Aside
from not requiring an explicit port handle, this function is identical to
[IOPort](/docs/IOPort)'s Read (see [IOPort](/docs/IOPort) Read? for more details).

Output:
serialData (1xN char).

\11/29/12    zlb   Wrote it based on the PR670Toolbox.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/PR705Toolbox/PR705read.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/PR705Toolbox/PR705read.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/PR705Toolbox/PR705read.m</code>
</div>
