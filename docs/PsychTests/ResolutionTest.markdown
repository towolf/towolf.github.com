---
layout: mfile
title: ResolutionTest
categories:
  - PsychTests
encoding: UTF-8
---

ResolutionTest prints screen resolutions reported by [Screen](/docs/Screen) 'Resolution'
and 'Resolutions'.

Usage: ResolutionTest([screenNumbers=all]);

On Linux, if a Psychtoolbox screen (=X-[Screen](/docs/Screen)) has multiple video outputs
attached, this function will report both, per output settings and modes and
the unified resolution of a screen - consisting of virtual resolutions and
settings formed by all attached outputs. Per-Output settings on Linux can
be made via [Screen](/docs/Screen)('ConfigureDisplay', 'Scanout', screenNumber, outputNumber, ...);
[Screen](/docs/Screen)('Resolution', screenNumber, ...); only affects or reports the unified
"virtual resolution" of a whole X-[Screen](/docs/Screen), not of its individual outputs.

Also see SetResolution, NearestResolution, and [Screen](/docs/Screen) Resolution and Resolutions.
