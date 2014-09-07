---
layout: mfile
title: GetEchoNumber
categories:
  - PsychOneliners
encoding: UTF-8
---

number = GetEchoNumber\(window, msg, x, y \[, textColor\]\[, bgColor\]\[, deviceIndex\]\[, untilTime=inf\]\[, KbCheck args...\]\)

Get a number typed at the keyboard. Entry is terminated by <return\> or
<enter\>. Typed characters are displayed on the screen. Useful for i/o in
a [Screen](/docs/Screen) window. Equivalent to "number = str2num\(GetEchoString\(...\)\)".

Returns the empty matrix if no number is entered. Returns a column vector
with multiple numbers if more than one number is entered.

Typed characters are displayed in the window. The delete or backspace key
is handled correctly, ie., it erases the last typed number.

'window' = Window to draw to. 'msg' = A message string displayed to
prompt for input. 'x', 'y' = Start position of message prompt.
'textColor' = Color to use for drawing the text. 'bgColor' = Background
color for text. By default, the background is transparent. If a non-empty
'bgColor' is specified it will be used. The current alpha blending
setting will affect the appearance of the text if 'bgColor' is specified\!

See also: GetNumber, GetString, GetEchoString


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetEchoNumber.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetEchoNumber.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetEchoNumber.m</code>
</div>
