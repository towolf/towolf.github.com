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
installed, as this is required for [Screen](/docs/Screen)() multi-media functions to
work. It performs [GStreamer](/docs/GStreamer) setup, or outputs a warning if the runtime is
missing.

This function is normally called from the startup.m Matlab startup file.
