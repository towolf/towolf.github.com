---
layout: mfile
title: PR705init
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705init - Initialize the serial port to talk to the PR-705.

Syntax:
retval = PR705init
retval = PR705init(portString)

Description:
Initializes the serial port and establishes remote mode for the PR-705.

Input:
portString (1xN char) - Name of the serial port to use.

Output:
response (1xN char) - Character data returned from the PR-705.

\11/29/12    zlb   Wrote it based on the PR670Toolbox.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/PR705Toolbox/PR705init.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/PR705Toolbox/PR705init.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/PR705Toolbox/PR705init.m</code>
</div>
