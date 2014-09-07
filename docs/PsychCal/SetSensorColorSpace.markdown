---
layout: mfile
title: SetSensorColorSpace
categories:
  - PsychCal
encoding: UTF-8
---

[cal,errorRet] = SetSensorColorSpace(cal, T\_sensor, S\_sensor, [quiet])

Initialize the sensor color space for use in calibration.  Requires
a calibration structure which contains the standard
fields.  These are checked for and a message is printed if
they are not there.

Checks that wavelength sampling is consistent and splines
if not.

errorRet indicates status of the operation.
  \== 0: OK
  \== 1: Bad condition number on linear/device conversion matrix

quiet flag suppresses error messages, default 0.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychCal/SetSensorColorSpace.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychCal/SetSensorColorSpace.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychCal/SetSensorColorSpace.m</code>
</div>
