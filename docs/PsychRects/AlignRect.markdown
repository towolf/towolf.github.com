---
layout: mfile
title: AlignRect
categories:
  - PsychRects
encoding: UTF-8
---

rect=AlignRect(rect,fixedRect,side1,[side2])  

Moves rect to align its center/top/bottom/left/right with the  
corresponding edge(s)/point of fixedRect. Does "side1" and then "side2".  
The legal values for side1 and side2 are 'center', 'left', 'right',  
'top', and 'bottom'.  
     r=AlignRect(r,screenRect,'center','top');  
For backward compatibility, also accepts 1,2,3,4,5. You may use the  
pre-defined constants RectLeft,RectRight,RectTop,RectBottom, but there is  
no named constant for centering.  
Also see PsychRects.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRects/AlignRect.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRects/AlignRect.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRects/AlignRect.m</code>
</div>
