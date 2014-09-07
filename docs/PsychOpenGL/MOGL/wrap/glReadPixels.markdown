---
layout: mfile
title: glReadPixels
categories:
  - wrap
encoding: UTF-8
---

glReadPixels  Interface to OpenGL function glReadPixels

usage:
For standard readback into a Matlab or Octave image matrix:
retpixels = glReadPixels\( x, y, width, height, format, type \)

For readback into the currently bound OpenGL Pixelbuffer object \(PBO\):
glReadPixels\( x, y, width, height, format, type, bufferoffset \)
where bufferoffset is the positive integer byte-offset into the PBO.

C function:  void glReadPixels\(GLint x, GLint y, GLsizei width, GLsizei height, GLenum format, GLenum type, GLvoid\* retpixels\)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/glReadPixels.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/glReadPixels.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/glReadPixels.m</code>
</div>
