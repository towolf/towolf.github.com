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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/moglputbuffer.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/moglputbuffer.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/moglputbuffer.m</code>
</div>
