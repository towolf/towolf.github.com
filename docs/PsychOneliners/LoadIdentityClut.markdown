---
layout: mfile
title: LoadIdentityClut
categories:
  - PsychOneliners
encoding: UTF-8
---

oldClut = LoadIdentityClut(windowPtr [, loadOnNextFlip=0][, lutType=auto][, disableDithering=1])  

Loads an identity clut on the window specified by windowPtr. If  
loadOnNextFlip is set to 1, then the clut will be loaded on the next call  
to [Screen](/docs/Screen)('[Flip](/docs/Flip)'). By default, the clut will be loaded immediately or on  
the next vertical retrace, depending on OS and graphics card.  
By default, also tries to disable digital output dithering on supported  
hardware, setting the optional flag 'disableDithering' to zero will  
leave dithering alone.  

If you use Linux and have low level hardware access enabled via a call  
to PsychLinuxConfiguration during installation or later, or if you  
use OS/X and have the PsychtoolboxKernelDriver loaded  
("help PsychtoolboxKernelDriver") and the graphics card is a GPU of the  
ATI/AMD Radeon X1000 series or a HD series card (e.g., HD-2000) or a  
equivalent model of the FireGL or FirePro series, then this routine will  
try to use special low-level setup code for optimal identity mapping. It  
will also disable digital display dithering if disableDithering == 1.  
On Windows with AMD cards, digital display dithering will also get disabled  
automatically. On other graphics cards, digital display dithering will not  
be affected.  

On other than AMD cards under Linux or OSX, the function will make  
a best effort to upload a suitable clut, as follows:  

This mechanism relies on heuristics to detect the exact type of LUT to  
upload into your graphics card. These heuristics may go wrong, thanks to  
the ever increasing amount of graphics hardware driver bugs in both  
Windows and MacOS/X. For that reason you can also use the function  
SaveIdentityClut() to manually specify either the type of LUT to use  
(overriding the automatic choice), or to specify the complete LUT, or to  
capture the current identity LUT of a display that works. That function  
will store the override Clut in a per-user, per-GPU, per-[Screen](/docs/Screen) configuration  
file. If LoadIdentityClut finds such a matching configuration file, it  
will use the LUT specified there, instead of performing an automatic  
selection.  

The routine optionally returns the old clut in 'oldClut'.  

You can restore the old "original" LUT at any time by calling  
RestoreCluts, or [sca](/docs/sca), but only until you call clear all! The original  
LUT's are backed up in a global variable for this to work.  

If you use a Cambridge Research systems Bits+ or Bits# box or a VPixx Inc.  
DataPixx, ViewPixx or ProPixx device, use the script BitsPlusIdentityClutTest  
for advanced diagnostic and troubleshooting wrt. identity clut's, display  
dithering and other evils which could spoil your day for high bit depth  
visual stimulus display.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/LoadIdentityClut.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/LoadIdentityClut.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/LoadIdentityClut.m</code>
</div>
