---
layout: mfile
title: GL_SRC_ALPHA_SATURATE
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

constantString=GL\_SRC\_ALPHA\_SATURATE  

Return the string 'GL\_SRC\_ALPHA\_SATURATE', which specifies an alpha  
blending factor to [Screen](/docs/Screen)('BlendFunction', ...).  

"Alpha" is a factor which weights RGB values when combining pixels by  
drawing or copying.  Alpha values weight the pixels drawn, the "source  
surface".   Separate alpha values weight the pixels drawn onto, the  
"destination surface".   A given pixel's alpha factor is not necessarily  
the alpha component of that pixel's [rgba] color vector, but may instead  
be the other combined surface's alpha component, a function of either or  
both both alpha compoenents, a constant, or it may derive from RGB values  
of the other combined surface.  The Psychtoolbox command  
[Screen](/docs/Screen)('BlendFunction') selects which. It implements the OpenGL function  
"glBlendFunc".  

In MATLAB, [Screen](/docs/Screen)('BlendFunction') accepts strings named for C constants  
passed to the OpenGL function glBlendFunc().Enter "Help  
PsychAlphaBlending" in the MATLAB command window for a list of blending  
constants (and other functions related to alpha blending).  

GL\_SRC\_ALPHA\_SATURATE may only be used as a source factor, not a  
destination factor.  

see also: PsychAlphaBlending, AlphaDemo, TestAlphaBlending.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychAlphaBlending/GL_SRC_ALPHA_SATURATE.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychAlphaBlending/GL_SRC_ALPHA_SATURATE.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychAlphaBlending/GL_SRC_ALPHA_SATURATE.m</code>
</div>
