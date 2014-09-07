---
layout: mfile
title: SimpleStepExperiment
categories:
  - Palmerdemo_notOSXed
encoding: UTF-8
---

Simple experiment to measure response time using eye movements.
v10 new improved single condition experiment (like e3, e5)
Displays fixation followed by left or right stimulus.
Requires left or right eye movement to corresponding stimulus.
Requires file:  setEyelinkDefaults
John Palmer, last revised 6/6/01

\2/21/01 v1: based on crt1
\2/26/01 v2: modifed to provide messages for asc2fira data file conversion
\2/28/01 added code to pass messages with stimulus location
\3/1/01  revised side message to use time stamps, added breaks
\3/17/01 added receivefile and changed to update current directory
\3/20/01 v3: simplified file i/o, record only during trial, sets resolution
\3/21/01 reworked header and messages, don't save .mat file at all
\3/27/01 moved all key messages to after DISPLAY\_ON
\4/2/01  added condition vector and message
\4/6/01  v4: introduced multiple conditions, varies ecc of target
\4/10/01 fixed bug with lower case condition message
\4/11/01 increased stimulus duration to 1.0 s
\4/13/01 v5: cut back to one condition keeping improvements
\5/2/01  v5a:  changed resolution
\5/3/01  updated h.pixelsperdegree to 25.5 and other sizes
\5/25/01 v5t:  modified for eyelinktoolbox v1.0, no receivefile
\6/4/01  put receivefile back in
\6/6/01  v10:  updated for eyelinktoolbox 1.1, added calibration

bugs
pause key only tested for at beginning of trial


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/EyelinkToolbox/EyelinkDemos/notOSXed/Palmerdemo_notOSXed/SimpleStepExperiment.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/EyelinkToolbox/EyelinkDemos/notOSXed/Palmerdemo_notOSXed/SimpleStepExperiment.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/EyelinkToolbox/EyelinkDemos/notOSXed/Palmerdemo_notOSXed/SimpleStepExperiment.m</code>
</div>
