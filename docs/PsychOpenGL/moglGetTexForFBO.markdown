---
layout: mfile
title: moglGetTexForFBO
categories:
  - PsychOpenGL
encoding: UTF-8
---

texid = moglGetTexForFBO(fbo, bufferid) -- Return texture name of texture which is
bound to the specified 'fbo' Framebuffer object as color buffer number 'bufferid'.
bufferid defaults to 1, aka the first attached color buffer.