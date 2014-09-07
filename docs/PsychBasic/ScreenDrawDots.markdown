---
layout: mfile
title: ScreenDrawDots
categories:
  - PsychBasic
encoding: UTF-8
---

Workaround-Wrapper for the [Screen](/docs/Screen)('DrawDots') function.  

Usage: ScreenDrawDots(windowPtr, xy [, dotdiameter=1][, dotcolor=white][, center2D][, dot\_type=1]);  

This function is the equivalent of the [Screen](/docs/Screen)('DrawDots') subfunction  
for fast drawing of 2D dots. It has the same parameters as that function,  
so it can be used as a drop-in replacement in many cases.  

On most systems, this function will simply call [Screen](/docs/Screen)('DrawDots',...);  
passing it all parameters you provided, so you'll get exactly that  
functionality, minus a little bit of performance loss due to the extra  
call overhead.  

On severely broken systems (like the piece of junk that Apple calls Snow  
Leopard 10.6.3), where the iPhone company managed to screw up their OpenGL  
implementation so badly that even [Screen](/docs/Screen)('DrawDots') doesn't work, it  
will try to use a different method to emulate 'DrawDots' behaviour as  
closely as possible. This is a hack! It will incur significant  
performance loss and it will provide an imperfect emulation which  
should work ok for simple cases of usage of 'DrawDots', but may not work  
perfectly (or at all) for complex usage or with high precision framebuffers.  

For syntax and further help, see help of "[Screen](/docs/Screen) DrawDots?"  

To replace direct calls to [Screen](/docs/Screen)('DrawDots',...); with calls to this  
function, simply use text search & replace of your text editor to search  
for:  
      [Screen](/docs/Screen)('DrawDots'  

# and set the replace text to:  

      ScreenDrawDots(  


You can enable the workaround (across sessions) via a call:  
clear all; ScreenDrawDots(1); on the Matlab/Octave command line.  

You can disable the workaround (across sessions) via a call:  
clear all; ScreenDrawDots(0); on the Matlab/Octave command line.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/ScreenDrawDots.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/ScreenDrawDots.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/ScreenDrawDots.m</code>
</div>
