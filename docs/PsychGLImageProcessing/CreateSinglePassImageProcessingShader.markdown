---
layout: mfile
title: CreateSinglePassImageProcessingShader
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

Create a single-pass image processing shader for direct use with [Screen](/docs/Screen)('DrawTexture')  

# Usage:  

[shader, varargout] = CreateSinglePassImageProcessingShader(windowPtr, shaderType, varargin)  

Creates a shader for window 'windowPtr' of type 'shaderType' with  
optional, type specific, parameters. Returns a handle 'shader' and  
optional other properties.  

# The following types are currently supported:  

'BackgroundMaskOut':  
--------------------  

 shader = CreateSinglePassImageProcessingShader(windowPtr, 'BackgroundMaskOut', backgroundColor [, tolerance]);  
 - This shader draws a texture, but removes all "backgroundColor" pixels  
 during drawing, effectively masking them out. 'backgroundColor' is a 3  
 component [R, G, B] vector with the RGB color values of the color to be  
 considered a background to remove. All color values around an euclidean  
 distance of 'tolerance' in 3D color space around the backgroundColor are  
 considered background color. The default tolerance is 0.001 units, which  
 for 8 bit colors means a perfect match -- zero tolerance.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/CreateSinglePassImageProcessingShader.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/CreateSinglePassImageProcessingShader.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/CreateSinglePassImageProcessingShader.m</code>
</div>
