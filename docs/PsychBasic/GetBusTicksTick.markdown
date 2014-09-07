---
layout: mfile
title: GetBusTicksTick
categories:
  - PsychBasic
encoding: UTF-8
---

busTickPeriod = GetBusTicksTick

# OS X

Return the period of the GetBusTicks clock.  The period of the
GetBusTicks clock depends on your model of CPU and its clock speed.
For reliable high-precision timing in standard units of seconds use
GetSecs instead of GetBusTicks.

GetBusTicksTick returns the period of the GetBusTicks clock.  The
frequency is found in the hw.busfreq field of the struct returned by
[Screen](/docs/Screen)('Computer').

# OS 9

GetBusTicksTick does not exist in OS 9.

# WINDOWS

GetBusTicksTick does not exist in Windows.
----

SEE ALSO: GetBusTicks, GetSecs, GetSecsTick, [Screen](/docs/Screen)('Computer')