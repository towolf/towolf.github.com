---
layout: mfile
title: AddToGLOperator
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

AddToGLOperator\(gloperator, opname, shaderhandle \[, blittercfg\] \[, luttexid\]\)

Add additional GLSL image processing shaders to GL operator 'gloperator'.

'opname' is the name of the to be added shader -- purely for debug
purpose.

'shaderhandle' is the GLSL handle of the shader to add.

'blittercfg' is the optional blitter configuration string with special
parameters.

'luttexid' is the optional numeric OpenGL handle of a texture for use as
lookup-table.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/AddToGLOperator.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/AddToGLOperator.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/AddToGLOperator.m</code>
</div>
