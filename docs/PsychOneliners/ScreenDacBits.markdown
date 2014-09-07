---
layout: mfile
title: ScreenDacBits
categories:
  - PsychOneliners
encoding: UTF-8
---

dacBits = ScreenDacBits(windowPtrOrScreenNumber)  

What is the precision of the DACs on this graphics card?  

At present you need to know the bit depth of your graphics board's DAC  
to determine how to write its CLUT, i.e. [Screen](/docs/Screen) 'SetClut' or 'Gamma'.  
Use this routine and ScreenUsesHighGammaBits, instead of the the brand-  
and platform-specific IsRadiusThunder10 and IsATIRadeon10, to keep your  
program as general as possible, not tied to particular hardware or  
platform.  

The value is set in PrepareScreen.m.  

See also LoadClut, ScreenPixelSize, ScreenUsesHighGammaBits, ScreenClutSize.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/ScreenDacBits.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/ScreenDacBits.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/ScreenDacBits.m</code>
</div>
