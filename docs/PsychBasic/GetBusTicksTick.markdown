---
layout: mfile
title: GetBusTicksTick
categories:
  - PsychBasic
encoding: UTF-8
---

busTickPeriod = GetBusTicksTick

OS X: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Return the period of the GetBusTicks clock.  The period of the
GetBusTicks clock depends on your model of CPU and its clock speed.
For reliable high-precision timing in standard units of seconds use
GetSecs instead of GetBusTicks.

GetBusTicksTick returns the period of the GetBusTicks clock.  The
frequency is found in the hw.busfreq field of the struct returned by
[Screen](/docs/Screen)\('Computer'\).

OS 9: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

GetBusTicksTick does not exist in OS 9.

WINDOWS: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

GetBusTicksTick does not exist in Windows.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

SEE ALSO: GetBusTicks, GetSecs, GetSecsTick, [Screen](/docs/Screen)\('Computer'\)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/GetBusTicksTick.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/GetBusTicksTick.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/GetBusTicksTick.m</code>
</div>
