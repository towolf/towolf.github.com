---
layout: mfile
title: OMLBasicTest
categories:
  - PsychTests
encoding: UTF-8
---

OMLBasicTest([screenid=max]) - Test basic correctness of OpenML timestamping.  

Performs a sequence of 300 flips, acquires timestamps of  
[Flip](/docs/Flip) completion according to OML\_sync\_control timestamping,  
as well as a post-swap GetSecs timestamp and a timestamp of  
the last vblank. If OpenML timestamping works correctly, then  
all three timestamps should be almost identical, ie., the vblank  
and flip timestamps should be identical, the GetSecs timestamp  
only minimally later than the flip timestamp, depending on  
system scheduling noise and load.  

If the timestamps (minus a few outliers) disagree, then  
something is likely broken in OpenML flip timestamping.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychTests/OMLBasicTest.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychTests/OMLBasicTest.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychTests/OMLBasicTest.m</code>
</div>
