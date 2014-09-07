---
layout: mfile
title: moglDeleteFBO
categories:
  - PsychOpenGL
encoding: UTF-8
---

moglDeleteFBO(fbo) -- Delete FBO 'fbo' and its associated buffers and textures.

This function is mostly useful for image processing and GPGPU
applications. Normal Psychtoolbox code will want to use standard
Offscreen windows instead. They are properly managed by Psychtoolbox for
normal stimulus drawing and implemented to work on any kind of hardware,
whereas this function is optimized for OpenGL-2 compliant hardware.