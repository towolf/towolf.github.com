---
layout: mfile
title: moglcalloc
categories:
  - wrap
encoding: UTF-8
---

ptr = moglcalloc(nelements, nrbytes) -- Allocate a memory buffer inside mogl.
This function allocates an internal memory buffer inside mogl for use
with OpenGL functions that use buffers for passing data forth and back
between Matlab and OpenGL, e.g., glFeedbackBuffer() or glSelectBuffer().

The allocated memory buffer is filled with zeros, just like the C-Function
calloc() would do.

nelements = The number of elements to allocate.
nrbytes = The number of bytes for each element to allocate.

-> nelements \* nrbytes will be allocated.

On successfull allocation, ptr will be a handle for the memory buffer.
You can think of ptr as a memory pointer in the C-language.

moglcalloc()'ed memory buffers can be released - one by one - via
moglfree(ptr), all at once via moglfreeall, and they are automatically
released when moglcore is clear'ed via clear moglcore, clear mex or
clear all.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/moglcalloc.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/moglcalloc.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/moglcalloc.m</code>
</div>
