---
layout: mfile
title: GetKbChar
categories:
  - PsychOneliners
encoding: UTF-8
---

[ch, when] = GetKbChar([deviceIndex][, untilTime=inf][, optional KbCheck arguments...]);

GetKbChar reimplements basic functionality of GetChar() by use of KbCheck
and KbPressWait. It accepts optionally all arguments that KbCheck accepts
and passes those arguments to KbCheck, e.g., a keyboard index in order to
only query a specific keyboard for input.

GetKbChar also returns with empty return values if the optional deadline
'untilTime' is reached.

The function only recognizes standard alpha-numeric keys, i.e., letters
and numbers, and a few special symbols like the ones on top of the
numeric keys. It only recognizes the delete, space and return keys as
special function keys, not other keys like Function keys, CTRL, ALT or
cursor keys. It always assumes a US keyboard mapping.

It polls the keyboard, so may miss very brief keystrokes and doesn't use
the keyboard queue.

Use this function if you need a GetChar like interface for simple string
and number input in situations where GetChar doesn't work reliably, e.g.,
on some Octave configurations, with Matlab in -nojvm mode or on
MS-Windows Vista or Windows-7.
