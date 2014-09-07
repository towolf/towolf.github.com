---
layout: mfile
title: IsPsychStartupImplantedInStartup
categories:
  - PsychInitialize
encoding: UTF-8
---

isImplanted = IsPsychStartupImplantedInStartup

Return TRUE if both the startup.m file is on the MATLAB path and if it
includes a call to PsychStartup.

If you have your own startup.m file which you want to use, then place it
ahead of the Psychtoolbox startup.m file on MATLAB's search path and add
to your file the line:
  PsychStartup; % Setup Psychtoolbox.
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychInitialize/IsPsychStartupImplantedInStartup.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychInitialize/IsPsychStartupImplantedInStartup.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychInitialize/IsPsychStartupImplantedInStartup.m</code>
</div>
