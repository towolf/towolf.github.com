---
layout: mfile
title: GetGamepadIndices
categories:
  - PsychHardware
encoding: UTF-8
---

keyboardIndices = GetGamepadIndices

# OS X

PsychHID assigns each USB HID device connected to you computer a
unique index. GetGamepadIndices returns the indices for those HID devices
which are gamepads.  The product names of each gamepad are returned in a
second argument which is useful to identify the gamepad associated with
an index.  For complete information on a gampad use PsychHID\('Devices'\).

# OS 9

GetGamepadIndices does not exist in OS 9.

# WINDOWS

GetGamepadIndices does not exist in Windows.
----

see also: GetKeyboardIndices


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/GetGamepadIndices.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/GetGamepadIndices.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/GetGamepadIndices.m</code>
</div>
