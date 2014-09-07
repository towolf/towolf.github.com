---
layout: mfile
title: glGetProgramResourceiv
categories:
  - wrap
encoding: UTF-8
---

glGetProgramResourceiv  Interface to OpenGL function glGetProgramResourceiv

usage:  [ length, params ] = glGetProgramResourceiv( program, programInterface, index, propCount, props, bufSize )

C function:  void glGetProgramResourceiv(GLuint program, GLenum programInterface, GLuint index, GLsizei propCount, const GLenum\* props, GLsizei bufSize, GLsizei\* length, GLint\* params)