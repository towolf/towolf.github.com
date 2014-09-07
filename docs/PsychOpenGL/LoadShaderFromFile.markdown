---
layout: mfile
title: LoadShaderFromFile
categories:
  - PsychOpenGL
---

handle = LoadShaderFromFile\(filename \[, shadertype\] \[, debug\]\)

Loads a GLSL OpenGL shader definition from textfile 'filename' and
creates an OpenGL GLSL shader of type 'shadertype'. Returns a handle to
the new shader. If shadertype is omitted, the type of the shader is
derived from the filename extension: .vert == GL\_VERTEX\_SHADER, .frag ==
GL\_FRAGMENT\_SHADER, .geom == GL\_GEOMETRY\_SHADER, .tesscontrol =
GL\_TESS\_CONTROL\_SHADER, .tesseval = GL\_TESS\_EVALUATION\_SHADER. The
optional 'debug' flag allows to enable debugging output.

On successfull load & creation, a 'handle' to the new shader is returned.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/LoadShaderFromFile.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/LoadShaderFromFile.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/LoadShaderFromFile.m</code>
</div>
