---
layout: mfile
title: glGetDebugMessageLog
categories:
  - wrap
encoding: UTF-8
---

glGetDebugMessageLog  Interface to OpenGL function glGetDebugMessageLog

usage:  [ r, sources, types, ids, severities, lengths, messageLog ] = glGetDebugMessageLog( count, bufsize )

C function:  GLuint glGetDebugMessageLog(GLuint count, GLsizei bufsize, GLenum\* sources, GLenum\* types, GLuint\* ids, GLenum\* severities, GLsizei\* lengths, GLchar\* messageLog)