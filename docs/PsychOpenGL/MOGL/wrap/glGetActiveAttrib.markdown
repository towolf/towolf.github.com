---
layout: mfile
title: glGetActiveAttrib
categories:
  - wrap
encoding: UTF-8
---

glGetActiveAttrib  Interface to OpenGL function glGetActiveAttrib

usage:  [ length, size, type, name ] = glGetActiveAttrib( program, index, bufSize )

C function:  void glGetActiveAttrib(GLuint program, GLuint index, GLsizei bufSize, GLsizei\* length, GLsizei\* size, GLenum\* type, GLchar\* name)