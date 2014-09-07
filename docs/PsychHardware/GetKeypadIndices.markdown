---
layout: mfile
title: GetKeypadIndices
categories:
  - PsychHardware
encoding: UTF-8
---

keypadIndices= GetKeypadIndices

# OS X

The PsychHID assigns each USB HID device connected to you computer a
unique index. GetKeypadIndices returns the indices for those HID
devices which are keypads.  The product names of each keypad are
returned in a second argument which is useful to identify the keypad
associated with an index.  For complete information on a keypad use
PsychHID('Devices').

# OS 9

GetKeypadIndices does not exist in OS 9.

# WINDOWS

GetKeypadIndices does not exist in Windows.
----

see also: GetGamepadIndices, GetKeyBoardIndices