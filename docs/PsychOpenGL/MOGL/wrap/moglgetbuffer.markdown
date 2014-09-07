---
layout: mfile
title: moglgetbuffer
categories:
  - wrap
encoding: UTF-8
---

outmatrix = moglgetbuffer(ptr, mattype, nrbytes) -- Copy content of buffer to matrix.

This creates a matrix of type 'mattype' and size 'nrbytes' bytes and then
copies the content of memory buffer 'ptr' into the matrix. The matrix is
then returned. ptr needs to be a handle to a buffer previously created via
ptr=moglmalloc() or ptr = moglcalloc(...). At most nrbytes are copied - if
the source buffer is too small for nrbytes, only the amount is copied thats
contained in the buffer.

mattype can be currently one of:
GL.DOUBLE - for double values, GL.UNSIGNED\_INT - for 32 bit unsigned integers.
GL.UNSIGNED\_BYTE - for unsigned bytes, aka uint8 values.
