---
layout: mfile
title: glGetDebugMessageLogARB
categories:
  - wrap
encoding: UTF-8
---

glGetDebugMessageLogARB  Interface to OpenGL function glGetDebugMessageLogARB

usage:  [ r, sources, types, ids, severities, lengths, messageLog ] = glGetDebugMessageLogARB( count, bufsize )

C function:  GLuint glGetDebugMessageLogARB(GLuint count, GLsizei bufsize, GLenum\* sources, GLenum\* types, GLuint\* ids, GLenum\* severities, GLsizei\* lengths, GLchar\* messageLog)