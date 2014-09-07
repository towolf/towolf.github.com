---
layout: mfile
title: glMultiDrawElementsBaseVertex
categories:
  - wrap
encoding: UTF-8
---

glMultiDrawElementsBaseVertex  Interface to OpenGL function glMultiDrawElementsBaseVertex

usage:  glMultiDrawElementsBaseVertex( mode, count, type, indices, drawcount, basevertex )

Note: indices must be a cell array whose cells contain uint32() type
vectors with the indices!

C function:  void glMultiDrawElementsBaseVertex(GLenum mode, const GLsizei\* count, GLenum type, const GLvoid\*\* indices, GLsizei drawcount, const GLint\* basevertex)