---
layout: mfile
title: moglputbuffer
categories:
  - wrap
encoding: UTF-8
---

moglputbuffer(inputmatrix, ptr, nrbytes) -- Copy content of matrix to buffer.

This copies the content of the matrix 'inputmatrix' into the mogl memory
buffer 'ptr' which was previously created via calls to ptr = moglmalloc(...)
or ptr = moglcalloc(...). At most nrbytes are copied - if the target buffer
is too small for nrbytes, only the amount is copied that fits into the buffer.

Be careful to avoid setting nrbytes to a size that exceeds the size of
inputmatrix, or Matlab/Octave will possibly crash or do other nasty things!