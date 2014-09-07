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
retpixels = glReadPixels( x, y, width, height, format, type )

For readback into the currently bound OpenGL Pixelbuffer object (PBO):
glReadPixels( x, y, width, height, format, type, bufferoffset )
where bufferoffset is the positive integer byte-offset into the PBO.

C function:  void glReadPixels(GLint x, GLint y, GLsizei width, GLsizei height, GLenum format, GLenum type, GLvoid\* retpixels)