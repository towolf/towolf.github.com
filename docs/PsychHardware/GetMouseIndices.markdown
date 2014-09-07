---
layout: mfile
title: GetMouseIndices
categories:
  - PsychHardware
encoding: UTF-8
---

[mouseIndices, productNames, allInfo] = GetMouseIndices([typeOnly])

# OS X

PsychHID assigns each USB HID device connected to you computer a unique
index. GetMouseIndices returns the indices for those HID devices which
are mouses.  The product names of the mouses are returned in a second
argument which is useful to identify the mouse associated with a
paticular index.  For complete information on a gampad use
PsychHID('Devices').

# LINUX

GetMouseIndices allows selection of different types of pointing devices
via the optional 'typeOnly' argument:
'masterPointer' will only return indices of so called "master pointer"
devices. These correspond to visible mouse cursors.

# WINDOWS

GetMouseIndices works as on OS X.
----

see also: GetKeyboardIndices, GetKeypadIndices, GetGamepadIndices


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/GetMouseIndices.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/GetMouseIndices.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/GetMouseIndices.m</code>
</div>
