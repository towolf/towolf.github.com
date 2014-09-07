---
layout: mfile
title: CopyWindowTest
categories:
  - PsychTests
encoding: UTF-8
---

CopyWindowTest([uselegacy=0][, sf=1][, sd=1])

Basic correctness test of different path's of [Screen](/docs/Screen)('CopyWindow')
Copies a small rectangular region from one window into another window.
Each source region is copied/replicated 25 times into a 5 by 5 matrix.

Tested paths are:
Offscreen -\> Onscreen : This is the most often used (and fastest) path.
Offscreen -\> Offscreen: From an offscreen window to a different offscreen window.
Onscreen  -\> Onscreen : From one area of onscreen window to a different area.
Onscreen  -\> Offscreen: From an area of onscreen window into a offscreen window.

The current CopyWindow implementation has a couple of restrictions:
\* One can't copy from an offscreen window into the -same- offscreen window.
\* One can't copy from an onscreen window into a -different- onscreen window.
\* Sizes of sourceRect and targetRect need to match for Onscreen-\>Offscreen copy.
The optional [copyMode] argument is accepted but ignored.

Result of these test need to be checked via visual inspection and common sense.

Since the year 2012, Psychtoolbox uses fast offscreen window support from
the imaging pipeline by default, instead of the old legacy path, which was
less robust, slower, less flexible and more limited in its functionality (e.g.,
no support for floating point framebuffers, multi-sample anti-aliasing or
3D rendering with correct occlusion testing). The legacy path is only enabled
if your graphics card + driver does not support fast offscreen windows, or if
you manually force use of the legacy path by including the flag 2^24 as a
ConsereVRAMSetting, e.g., [Screen](/docs/Screen)('[Preference](/docs/Preference)', 'ConserveVRAM', 2^24);
See "help ConserveVRAMSettings", the section titled "kPsychDontAutoEnableImagingPipeline".

The only sensible reason to use the legacy path is if your graphics drivers
should have some bugs in handling of fast offscreen windows and a driver
update doesn't fix the problem. This CopyWindowTest() script should expose
such bugs. It also allows you to use test the legacy path with the optional
flag 'uselegacy' set to 1.
