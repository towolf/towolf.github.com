---
layout: mfile
title: BitsPlusEncodeClutRow
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

bitsPlusClutRow = BitsPlusEncodeClutRow(theClut)  

This is for the Cambridge Research Systems BITS++ 14-bit video DAC.  
BitsPlusEncodeClutRow accepts the desired content for the CLUT (color  
look up table) and encodes it so that it may be poked into the first (or  
last) line of the image. The BITS++ will detect the "unlock" code and  
transfer the CLUT data into the 256 entry, 3 channel, 14-bit CLUT.  
<http://www.crsltd.com/>


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/BitsPlusToolbox/BitsPlusEncodeClutRow.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/BitsPlusToolbox/BitsPlusEncodeClutRow.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/BitsPlusToolbox/BitsPlusEncodeClutRow.m</code>
</div>
