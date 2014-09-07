---
layout: mfile
title: GetEchoString
categories:
  - PsychOneliners
encoding: UTF-8
---

string = GetEchoString(window, msg, x, y, [textColor], [bgColor], [useKbCheck=0], [deviceIndex], [untilTime=inf], [KbCheck args...])  

Get a string typed at the keyboard. Entry is terminated by \<return\> or  
\<enter\>.  

Typed characters are displayed in the window. The delete or backspace key  
is handled correctly, ie., it erases the last typed character. Useful for  
i/o in a [Screen](/docs/Screen) window.  

'window' = Window to draw to. 'msg' = A message string displayed to  
prompt for input. 'x', 'y' = Start position of message prompt.  
'textColor' = Color to use for drawing the text. 'bgColor' = Background  
color for text. By default, the background is transparent. If a non-empty  
'bgColor' is specified it will be used. The current alpha blending  
setting will affect the appearance of the text if 'bgColor' is specified!  

If the optional flag 'useKbCheck' is set to 1 then KbCheck is used - with  
potential optional additional 'KbCheck args...' for getting the string  
from the keyboard. Otherwise GetChar is used. 'useKbCheck' == 1 is  
restricted to standard alpha-numeric keys (characters, letters and a few  
special symbols). It can't handle all possible characters and doesn't  
work with non-US keyboard mappings. Its advantage is that it works  
reliably on configurations where GetChar may fail, e.g., on MS-Vista and  
Windows-7.  

See also: GetNumber, GetString, GetEchoNumber  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetEchoString.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetEchoString.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetEchoString.m</code>
</div>
