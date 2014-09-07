---
layout: mfile
title: glGetBufferSubData
categories:
  - wrap
encoding: UTF-8
---

glGetBufferSubData  Interface to OpenGL function glGetBufferSubData

usage:  glGetBufferSubData( target, offset, dsize, data )

Caution: Caller needs to allocate 'data' as a matrix or vector of
suitable format and capacity for the data, otherwise bad things will
happen!

C function:  void glGetBufferSubData(GLenum target, GLint offset, GLsizei dsize, GLvoid\* data)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/glGetBufferSubData.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/glGetBufferSubData.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/glGetBufferSubData.m</code>
</div>
