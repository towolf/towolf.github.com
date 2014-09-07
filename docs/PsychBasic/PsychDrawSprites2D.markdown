---
layout: mfile
title: PsychDrawSprites2D
categories:
  - PsychBasic
encoding: UTF-8
---

Draw little texture in multiple places, with a similar syntax as  
[Screen](/docs/Screen)('DrawDots').  

Usage: PsychDrawSprites2D(windowPtr, spriteTex, xy [, spriteScale=1][, spriteAngle=0][, spriteColor=white][, center2D=[0,0]][, spriteShader]);  

This is basically a 'DrawDots' work-alike, just that it doesn't draw nice  
round dots, but many copies of nice little texture images, each  
individually colored, scaled, positioned, shaded and rotated.  

It is a convenience wrapper around the [Screen](/docs/Screen)('DrawTextures') command, a  
more low-level, more flexible command for drawing of many textures at  
once.  

'windowPtr' target window. 'spriteTex' texture to draw. 'xy' 2-row matrix  
with x,y locations of the centers of the drawn textures. 'center2D' adds  
an optional offset to these locations. 'spriteScale' global or per-sprite  
scaling factor. 'spriteAngle' global or per-sprite rotation angle.  
'spriteColor' global or per sprite 1-, 3- or 4-row color matrix.  
'spriteShader' a shader handle for shaded drawing.  

See [Screen](/docs/Screen) DrawTextures? for more help on the options and [Screen](/docs/Screen)  
DrawDots? for similar syntax. See DotDemo.m or DotDemo(1) for example  
usage.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/PsychDrawSprites2D.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/PsychDrawSprites2D.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/PsychDrawSprites2D.m</code>
</div>
