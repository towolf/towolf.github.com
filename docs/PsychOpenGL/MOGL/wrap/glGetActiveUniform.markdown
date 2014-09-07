---
layout: mfile
title: glGetActiveUniform
categories:
  - wrap
encoding: UTF-8
---

glGetActiveUniform  Interface to OpenGL function glGetActiveUniform

usage:  [ length, size, type, name ] = glGetActiveUniform( program, index, bufSize )

C function:  void glGetActiveUniform(GLuint program, GLuint index, GLsizei bufSize, GLsizei\* length, GLsizei\* size, GLenum\* type, GLchar\* name)