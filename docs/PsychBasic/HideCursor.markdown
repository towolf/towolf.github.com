---
layout: mfile
title: HideCursor
categories:
  - PsychBasic
encoding: UTF-8
---

HideCursor([screenid=0][, mouseid]

HideCursor hides the mouse cursor associated with screen 'screenid'.
By default, the cursor of screen zero on Linux, and all screens on
Windows and Mac OS/X is hidden. 'mouseid' defines which of multiple
cursors shall be hidden on Linux. The parameter is silently ignored
on other systems.
----

See ShowCursor, SetMouse