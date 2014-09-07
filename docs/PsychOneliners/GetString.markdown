---
layout: mfile
title: GetString
categories:
  - PsychOneliners
encoding: UTF-8
---

string = GetString([useKbCheck=0][, deviceIndex][, untilTime=inf][, optional KbCheck arguments...])

Get a string typed at the keyboard. Entry is terminated by
<return\> or <enter\>.

If the optional flag 'useKbCheck' is set to 1 then KbCheck is used - with
potential optional additional 'KbCheck args...' for getting the string
from the keyboard. Otherwise GetChar is used. 'useKbCheck' == 1 is
restricted to standard alpha-numeric keys (characters, letters and a few
special symbols). It can't handle all possible characters and doesn't
work with non-US keyboard mappings. Its advantage is that it works
reliably on configurations where GetChar may fail, e.g., on MS-Vista and
Windows-7.

Useful for i/o in a [Screen](/docs/Screen) window. Typed keys are not echoed.

See also: GetEchoString, GetNumber, GetEchoNumber



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetString.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetString.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetString.m</code>
</div>
