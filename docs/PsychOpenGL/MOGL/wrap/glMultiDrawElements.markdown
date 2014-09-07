---
layout: mfile
title: glMultiDrawElements
categories:
  - wrap
encoding: UTF-8
---

glMultiDrawElements  Interface to OpenGL function glMultiDrawElements

usage:  glMultiDrawElements( mode, count, type, indices, drawcount)

Note: indices must be a cell array whose cells contain uint32() type
vectors with the indices!

C function:  void glMultiDrawElements(GLenum mode, const GLsizei\* count, GLenum type, const GLvoid\*\* indices, GLsizei drawcount)