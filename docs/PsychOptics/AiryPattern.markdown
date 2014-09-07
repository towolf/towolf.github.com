---
layout: mfile
title: AiryPattern
categories:
  - PsychOptics
encoding: UTF-8
---

intensity = AiryPattern((angles,pupil,nm)

Compute the radial Airy pattern for diffraction by
a circular aperature.

  "angles" visual angle in radians
  "pupil" diameter in mm
  "nm" is wavelength in nm

Intensity is normalized to max of 1.

Formulae from Hecht, Optics, 2cd edition, p. 419.

\1/13/04  dhb  Wrote it.
\12/27/04 dhb    Deal with case of input == 0.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOptics/AiryPattern.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOptics/AiryPattern.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOptics/AiryPattern.m</code>
</div>
