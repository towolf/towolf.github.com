---
layout: mfile
title: PR670config
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670config - Update the PR-670 configuration.

Syntax:
configOUT = PR670config
configOUT = PR670config\(configIN\)

Description:
Updates the PR-670 configuration according to 'configIN'. If no input is
provided, returns the current configuration string. 'configIN' can be in
the form of the string returned from PR670config, or a cell containing values
ordered \{ Units, Exposure, N Samples, CIE Observer, Sync Mode, Frequency \}.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/PR670Toolbox/PR670config.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/PR670Toolbox/PR670config.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/PR670Toolbox/PR670config.m</code>
</div>
