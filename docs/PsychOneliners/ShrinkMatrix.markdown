---
layout: mfile
title: ShrinkMatrix
categories:
  - PsychOneliners
encoding: UTF-8
---

out = ShrinkMatrix(IN, FAC)  
Shrinks a 2-D or 3-D matrix IN (an image) by a factor FAC.  
matrix will be truncated horizontally and vertically so that the  
resultant shrunk matrix would have integer sizes in the x an y dimension.  
size of 3rd dimension will not be scaled.  
shrinking is performed by mean computation.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/ShrinkMatrix.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/ShrinkMatrix.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/ShrinkMatrix.m</code>
</div>
