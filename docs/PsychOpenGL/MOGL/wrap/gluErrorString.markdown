---
layout: mfile
title: gluErrorString
categories:
  - wrap
encoding: UTF-8
---

gluErrorString  Interface to gluErrorString

usage:  r = gluErrorString( err )
        r = gluErrorString

- with no input arguments, 'err' is obtained by calling glGetError

C function:  const GLubyte \* gluErrorString (GLenum error)