---
layout: mfile
title: DriftDemo5
categories:
  - PsychDemos
encoding: UTF-8
---

function DriftDemo5(angle, cyclespersecond, f, drawmask)
----

Display animated gratings using the new [Screen](/docs/Screen)('DrawTexture') command.

The demo shows two drifting sine gratings through circular apertures. The
\1st drifting grating is surrounded by an annulus (a ring) that shows a
second drifting grating with a different orientation.

The demo ends after a key press or after 20 seconds have elapsed.

The demo uses alpha-blending and color buffer masking for masking the
gratings with circular apertures.

# Parameters:

angle = Angle of the grating with respect to the vertical direction.
cyclespersecond = Speed of grating in cycles per second. f = Frequency of
grating in cycles per pixel.
drawmask = If set to 1, then a gaussian aperture is drawn over the grating
----

see also: PsychDemos, MovieDemo


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/DriftDemo5.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/DriftDemo5.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/DriftDemo5.m</code>
</div>
