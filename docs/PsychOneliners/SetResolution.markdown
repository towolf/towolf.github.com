---
layout: mfile
title: SetResolution
categories:
  - PsychOneliners
encoding: UTF-8
---

oldRes=SetResolution(screenNumber,width,height,[hz],[pixelSize])  
oldRes=SetResolution(screenNumber,res)  

Set the resolution of the screen.  This is intended to be used in  
programs that run psychophysical experiments, so SetResolution is  
strict. It issues a fatal error unless it can provide exactly the  
resolution you specified. (For lenience, look at NearestResolution.)  
"screenNumber" is the screen number.  
"width" and "height" are the desired dimensions in pixels.  
"hz" is the desired refresh rate (default is current frame rate).  
"pixelSize" 8, 16, 24, or 32 bits and defaults to current pixelSize.  
Returns the current resolution as "oldRes".  

  oldRes=SetResolution(0,1024,768,75);  
  w=[Screen](/docs/Screen)(0,'OpenWindow');  
  [Screen](/docs/Screen)(w,'PutImage',image);  
  [Screen](/docs/Screen)(w,'[Close](/docs/Close)');  
  SetResolution(0, oldRes);  

To display a list of available resolutions, try ResolutionTest. Also see  
NearestResolution, ResolutionTest, and [Screen](/docs/Screen)('Resolution')  
and [Screen](/docs/Screen)('Resolutions').  

NOTE: Apple has all the new LCD screens return a frame rate of 0, so  
we treat that value as a special case. A request for "hz" of NaN will  
match only with a frame rate of 0.  

NOTE: On Linux this only works as you'd expect if there is only one  
video output connected to a Psychtoolbox screen / X-[Screen](/docs/Screen). On a  
setup with multiple outputs per screen, this will only change the  
size of the framebuffer, but not the resolution of the actual displays!  
Use [Screen](/docs/Screen)('ConfigureDisplay', 'Scanout', ...); to change settings on  
such a multi-display per screen setup on Linux.  

Originally written by Sabina Wolfson.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/SetResolution.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/SetResolution.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/SetResolution.m</code>
</div>
