---
layout: mfile
title: MakeTextureDrawShader
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

glsl = MakeTextureDrawShader(windowPtr, shadertype [, backgroundColorOffset = [0,0,0,0]]);  

Create a special GLSL shader that can apply some special image processing  
operations that modify the normal drawing of textures via  
[Screen](/docs/Screen)('DrawTexture(s)'). Return a handle 'glsl' to the shader.  

The created shader can be attached to specific textures via passing the  
returned 'glsl' argument as the optional 'textureShader' argument for the  
[Screen](/docs/Screen)('MakeTexture', ....., textureShader); function. It can be also  
applied on a per-draw basis by passing the 'glsl' handle as optional  
'textureShader' argument to the [Screen](/docs/Screen)('DrawTexture(s)', ...); function.  


# Mandatory arguments:  

'windowPtr' A handle to the onscreen window to which the shader should be  
associated.  

'shadertype' A name string that defines the type of shader / image  
processing operation to apply. It can be one of the following:  

- 'SeparateAlphaChannel': Alpha values are looked up at the regular  
locations defined via the 'srcRect' parameter in a [Screen](/docs/Screen)('DrawTexture')  
call. RGB color values are looked up at srcRect, offset by some (dx,dy)  
offset, as provided by the 'auxParameters' vector [dx, dy, 0, 0].  
Providing non-zero offset values for dx and dy allows to "shift" or  
"scroll" the RGB or Luminance image inside a texture during drawing,  
while keeping the alpha image at a fixed location, solely defined by  
'srcRect'. This is mostly useful if you want to draw some drifting  
stimulus with a fixed alpha channel mask applied, ie., the color image  
should move, but the alpha mask should stay fixed.  

- 'PremultipliedAlphaChannel': Like 'SeparateAlphaChannel', but the alpha  
value is not written to the framebuffer, but premultiplied to the RGB  
color pixel before writeout.  

'backgroundColorOffset' Optional, defaults to [0 0 0 0]. A RGBA offset  
color to add to the final RGBA colors of the drawn texture, prior to  
drawing it.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/MakeTextureDrawShader.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/MakeTextureDrawShader.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/MakeTextureDrawShader.m</code>
</div>
