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
----