---
layout: mfile
title: glShaderSource
categories:
  - wrap
encoding: UTF-8
---

glShaderSource  Interface to glShaderSource

usage:  glShaderSource\(shader, shadersource, debug\)

This function differs from its C counterpart. You have to pass in the
handle of the shader as returned by glCreateShader in 'shader'.

You have to pass a single character string 'shadersource' that
contains the ASCII text of the shaders source code. Each line in the
string needs to be terminated by a '\\n' aka ASCII code 10 aka newline.
This string will be split up into the array of strings as expected by
the C function glShaderSource.

A simple way to read a shader from a standard text file is as follows:
fid=fopen\('MyShader.txt', 'r'\);
shadersource=fread\(fid\);
fclose\(fid\);
glShaderSource\(shader, shadersource\);

C function:  void glShaderSource\(GLuint shader, int numOfStrings, const char \*\*strings, int \*lenOfStrings\);


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/glShaderSource.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/glShaderSource.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/glShaderSource.m</code>
</div>
