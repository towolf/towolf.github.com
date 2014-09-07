---
layout: mfile
title: GetNumber
categories:
  - PsychOneliners
encoding: UTF-8
---

number = GetNumber([deviceIndex][, untilTime=inf][, optional KbCheck arguments...])

Get a number typed at the keyboard. Entry is terminated by
\<return\> or \<enter\>. Typed keys are not echoed. Useful for
i/o in a [Screen](/docs/Screen) window. Equivalent to "number=str2num(GetString)".

Returns the empty matrix if no number is entered. Returns a
column vector with multiple numbers if more than one number
is entered.

See also: GetEchoNumber, GetString, GetEchoString