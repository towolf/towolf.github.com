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