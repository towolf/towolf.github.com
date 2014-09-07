---
layout: mfile
title: PsychStartup
categories:
  - PsychInitialize
encoding: UTF-8
---

PsychStartup -- Perform Psychtoolbox related setup at Matlab/Octave startup.

This performs setup of Matlab or Octave at session startup for
Psychtoolbox.

On MS-Windows, it currently detects if the [GStreamer](/docs/GStreamer) 1.4+ runtime is
installed, as this is required for [Screen](/docs/Screen)\(\) multi-media functions to
work. It performs [GStreamer](/docs/GStreamer) setup, or outputs a warning if the runtime is
missing.

This function is normally called from the startup.m Matlab startup file.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychInitialize/PsychStartup.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychInitialize/PsychStartup.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychInitialize/PsychStartup.m</code>
</div>
