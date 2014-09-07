---
layout: mfile
title: glSelectBuffer
categories:
  - wrap
encoding: UTF-8
---

glSelectBuffer  Interface to OpenGL function glSelectBuffer  

usage:  glSelectBuffer( bufsize, bufferptr )  


bufsize = The number of unsigned int values that can be placed into the buffer.  

bufferptr = Pointer to a buffer created via bufferptr=moglmalloc() or  
            bufferptr=moglcalloc().  


For principle of usage, see help glFeedbackBuffer. This buffer is meant  
to be used when OpenGL is switched into glRenderMode(GL.SELECT).  

C function:  void glSelectBuffer(GLsizei bufsize, GLuint\* bufferptr)  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/glSelectBuffer.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/glSelectBuffer.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/glSelectBuffer.m</code>
</div>
