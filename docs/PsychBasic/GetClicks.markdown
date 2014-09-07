---
layout: mfile
title: GetClicks
categories:
  - PsychBasic
encoding: UTF-8
---

[clicks,x,y,whichButton] = GetClicks([windowPtrOrScreenNumber][, interclickSecs][, mouseDev])

Wait for the user to click the mouse, count the number of clicks
that occur within a inter-click interval of each other, and
then return the number of clicks and the mouse location, as well as the
numbers of the pressed buttons "whichButton".

The x,y location is the location at the downstroke of the first mouse
click. The mouse position (x,y) is "local", i.e. relative to the origin of
the window or screen, if supplied; otherwise it's "global", i.e. relative
to the origin of the main screen (the one with the menu bar).

The allowed inter-click interval can be adjusted by setting the Matlab
global variable "ptb\_mouseclick\_timeout" to a value in seconds. E.g.,
global ptb\_mouseclick\_timeout; ptb\_mouseclick\_timeout = 1; would set the
inter-click interval to 1 second. By default, the interval is 500 msecs.

You can also specify an override interval in the optional argument
'interClickSecs' for a given call to GetClicks. A setting of zero would
disable multi-click detection, ie., only wait for first mouse-click or
press, then return immediatly.

The optional 'mouseDev' parameter allows to select a specific mouse or
pointer device to query if your system has multiple pointer devices.
Currently Linux only, silently ignored on other operating systems.

See Also: GetMouse, SetMouse, GetMouseIndices