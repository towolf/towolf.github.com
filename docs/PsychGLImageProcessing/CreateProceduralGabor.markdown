---
layout: mfile
title: CreateProceduralGabor
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

[gaborid, gaborrect] = CreateProceduralGabor(windowPtr, width, height [, nonSymmetric=0][, backgroundColorOffset =(0,0,0,0)][, disableNorm=0][, contrastPreMultiplicator=1])  

Creates a procedural texture that allows to draw Gabor stimulus patches  
in a very fast and efficient manner on modern graphics hardware.  

This works on GPU's with support for the OpenGL shading language and  
vertex- and fragment shaders. See ProceduralGaborDemo and  
ProceduralGarboriumDemo for examples on how to use this function.  
ProceduralGaborDemo shows drawing of a single gabor and also allows to  
perform a speed benchmark and a correctness test to verify correct  
working and accuracy of this approach. ProceduralGarboriumDemo shows how  
to draw large numbers of gabor patches with different paramters in a very  
fast and efficient way.  

# Parameters and their meaning:  

'windowPtr' A handle to the onscreen window.  
'width' x 'height' The maximum size (in pixels) of the gabor. More  
precise, the size of the mathematical support of the gabor. Providing too  
small values here would 'cut off' peripheral parts or your gabor. Too big  
values don't hurt wrt. correctness or accuracy, they just hurt  
performance, ie. drawing speed. Use a reasonable size for your purpose.  

'nonSymmetric' Optional, defaults to zero. A non-zero value means that  
you intend to draw gabors whose gaussian hull is not perfectly circular  
symmetric, but a more general ellipsoid. The generated procedural texture  
will honor an additional 'spatial aspect ratio' parameter, at the expense  
of a higher computational effort and therefore slower drawing speed.  

'backgroundColorOffset' Optional, defaults to [0 0 0 0]. A RGBA offset  
color to add to the final RGBA colors of the drawn gabor, prior to  
drawing it.  

'disableNorm' Optional, defaults to 0. If set to a value of 1, the  
special multiplicative normalization term normf = 1/(sqrt(2\*pi) \* sc)  
will not be applied to the computed gabor. By default (setting 0), it  
will be applied. This term seems to be a reasonable normalization of the  
total amplitude of the gabor, but it is not part of the standard  
definition of a gabor. Therefore we allow to disable this normalization.  

'contrastPreMultiplicator' Optional, defaults to 1. This value is  
multiplied as a scaling factor to the requested contrast value. If you  
set the 'disableNorm' parameter to 1 to disable the builtin normf  
normalization and then specify contrastPreMultiplicator = 0.5 then the  
per gabor 'contrast' value will correspond to what practitioners of the  
field usually understand to be the contrast value of a gabor.  


The function returns a procedural texture handle 'gaborid' that you can  
pass to the [Screen](/docs/Screen)('DrawTexture(s)', windowPtr, gaborid, ...) functions  
like any other texture handle. The 'gaborrect' is a rectangle which  
describes the size of the gabor support.  

# A typical invocation to draw a single gabor patch may look like this:  

[Screen](/docs/Screen)('DrawTexture', windowPtr, gaborid, [], dstRect, Angle, [], [],  
modulateColor, [], kPsychDontDoRotation, [phase+180, freq, sc,  
contrast, aspectratio, 0, 0, 0]);  

Draws the gabor 'gaborid' into window 'windowPtr', at position 'dstRect',  
or in the center if 'dstRect' is set to []. Make sure 'dstRect' has the  
size of 'gaborrect' to avoid spatial distortions! You could do, e.g.,  
dstRect = OffsetRect(gaborrect, xc, yc) to place the gabor centered at  
screen position (xc,yc).  

The definition of the gabor mostly follows the definition of Wikipedia,  
but you can check the source code of ProceduralGaborDemo for a reference  
Matlab implementation which is exactly equivalent to what this routine  
does.  

Wikipedia's definition (better readable): http://en.wikipedia.org/wiki/Gabor\_filter  
See http://tech.groups.yahoo.com/group/psychtoolbox/message/9174 for  
Psychtoolbox forum message 9174 with an in-dephs discussion of this  
function.  


'Angle' is the optional orientation angle in degrees (0-360), default is zero degrees.  

'modulateColor' is the base color of the gabor patch - it defaults to  
white, ie. the gabor has only luminance, but no color. If you'd set it to  
[255 0 0] you'd get a reddish gabor.  

'phase' is the phase of the gabors sine grating in degrees.  

'freq' is its spatial frequency in cycles per pixel.  

'sc' is the spatial constant of the gaussian hull function of the gabor, ie.  
the "sigma" value in the exponential function.  

'contrast' is the amplitude of your gabor in intensity units - A factor  
that is multiplied to the evaluated gabor equation before converting the  
value into a color value. 'contrast' may be a bit of a misleading term  
here...  

'aspectratio' Defines the aspect ratio of the hull of the gabor. This  
parameter is ignored if the 'nonSymmetric' flag hasn't been set to 1 when  
calling the CreateProceduralGabor() function.  

Make sure to use the [Screen](/docs/Screen)('DrawTextures', ...); function properly,  
instead of the [Screen](/docs/Screen)('DrawTexture', ...); function, if you want to draw  
many different gabors simultaneously - this is much faster!  




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/CreateProceduralGabor.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/CreateProceduralGabor.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/CreateProceduralGabor.m</code>
</div>
