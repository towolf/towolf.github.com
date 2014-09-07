---
layout: mfile
title: CylToSensor
categories:
  - PsychCal
encoding: UTF-8
---

sensor = CylToSensor(cyl)

Convert from cylindrical to sensor coordinates.
We use the conventions of the CIE Lxx color spaces
for angle.  This inverts SensorToCyl, see that routine
for description of coordinate systems.

See also SensorToCyl, SensorToPolar, PolarToSensor.

10/17/93    dhb   Wrote it by converting CAP C code.
2/20/94     jms   Added single argument case to allow avoiding cData
4/5/02      dhb, ly  Change name.
11/6/06     dhb   Only allow one arg.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychCal/CylToSensor.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychCal/CylToSensor.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychCal/CylToSensor.m</code>
</div>
