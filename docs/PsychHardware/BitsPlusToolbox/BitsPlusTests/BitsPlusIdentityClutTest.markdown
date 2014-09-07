---
layout: mfile
title: BitsPlusIdentityClutTest
categories:
  - BitsPlusTests
encoding: UTF-8
---

Test signal transmission from the framebuffer to your CRS Bits+/Bits#  
device or VPixx Inc. DataPixx/ViewPixx device and similar CRS and VPixx  
products.  

Test proper function of the T-Lock mechanism, proper loading of identity  
gamma tables into the GPU, and for bad interference of dithering hardware  
with the DVI stream. This test is meant for Mono++ mode of Bits+, it  
won't work properly in any other mode!!  

Disclaimer: This test only exists because of the huge number of serious &  
embarassing bugs in the graphics drivers and operating systems from  
Microsoft, Apple, AMD and NVidia. All problems diagnosed here are neither  
defects in the Bits+ device or similar devices, nor Psychtoolbox bugs. As  
such, sadly they are mostly out of our control and there is only a  
limited number of ways we can try to help you to workaround the problems  
caused by miserable workmanship and insufficient quality control at those  
big companies.  

# Usage:  

BitsPlusIdentityClutTest([whichScreen=max][, usedpixx=0][, winrect=[]]);  

# How to test:  

1\. Make sure your Bits+ box is switched to Mono++ mode by uploading the  
   proper firmware. Or make sure your DataPixx is connected, both DVI  
   cable and USB cable.  

2\. Run the BitsPlusImagingPipelineTest script to validate that your  
   graphics card can create properly formatted images in the framebuffer  
   for Bits+ or DataPixx.  

3\. Run this script, optionally passing a screenid. It will test the  
   secondary display on a multi-display setup by default, or the external  
   display on a laptop. For a DataPixx device or similar, set the  
   optional 'usedpixx' flag to 1.  

If everything works, what you see onscreen should match the description  
in the blue text that is displayed.  

If a wrong gamma lut is uploaded into your GPU due to operating system  
and graphics driver bugs, you can try to toggle through different  
alternative lut's by repeatedly pressing the SPACE key and seeing if the  
display changes for the better. Should you find a setting that works, you  
can press the 's' key to save this configuration and Psychtoolbox will  
use this setting in all future sessions of your experiment scripts.  

You can exit the test by pressing the ESCape key, regardless if it was  
successfull or not.  

What could also happen is that you get a partial success: The display  
behaves roughly as described in the text, but you see the T-Lock color  
code line at the top of your display erratically appearing and  
disappearing - flickering. You also don't see a smooth animation of the  
drifting horizontal red gradient or a regular cycling of the "COLORFUL"  
words, but some jerky, irregular, jumpy animation, which may only update  
a few times per second, or even only once every couple seconds or at very  
irregular intervals. You may also see the display overlayed with random  
colorful speckles, or you may not see the gray background image and gray  
rotating gradient patch at all. In that case, the lut uploaded in your  
GPU may be correct, but due to some serious graphics driver or operating  
system bug, the GPU is applying spatial or temporal dithering to the  
video stream which will confuse the Bits+ and cause random artifacts and  
failure of the T-Lock mechanism.  

You should also double-check the cabling and connections to rule out  
connection problems and other defects.  

In that case, contact CRS support or check the Psychtoolbox Wiki for a  
workaround. Currently we have a workaround for MacOS/X systems, but not  
for MS-Windows systems.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/BitsPlusToolbox/BitsPlusTests/BitsPlusIdentityClutTest.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/BitsPlusToolbox/BitsPlusTests/BitsPlusIdentityClutTest.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/BitsPlusToolbox/BitsPlusTests/BitsPlusIdentityClutTest.m</code>
</div>
