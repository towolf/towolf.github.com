---
layout: mfile
title: glSelectBuffer
categories:
  - wrap
encoding: UTF-8
---

glSelectBuffer  Interface to OpenGL function glSelectBuffer

usage:  glSelectBuffer( bufsize, bufferptr )


bufsize = The number of unsigned int values that can be placed into the buffer.

bufferptr = Pointer to a buffer created via bufferptr=moglmalloc() or
            bufferptr=moglcalloc().


For principle of usage, see help glFeedbackBuffer. This buffer is meant
to be used when OpenGL is switched into glRenderMode(GL.SELECT).

C function:  void glSelectBuffer(GLsizei bufsize, GLuint\* bufferptr)