---
layout: mfile
title: GetMouseWheel
categories:
  - PsychBasic
encoding: UTF-8
---

wheelDelta = GetMouseWheel([mouseIndex])

Return change of mouse wheel position of a wheel mouse (in "wheel clicks")
since last query. 'mouseIndex' is the PsychHID device index of the wheel
mouse to query. The argument is optional: If left out, the first detected
real wheel mouse (ie. not a trackpad) is queried.

# OS X

Uses PsychHID for low-level access to mice with mouse wheels. If wheel
state is not queried frequent enough, the internal queue may overflow and
some mouse wheel movements may get lost, resulting in a smaller reported
'wheelDelta' than the real delta since last query. On OS X 10.4.11 the
operating system can store at most 10 discrete wheel movements before it
discards movement events.
----

# MS-Windows and Linux

This function is not (yet?) supported.
----
See also: GetClicks, GetMouseIndices, GetMouse, SetMouse, ShowCursor,
HideCursor
