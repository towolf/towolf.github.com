---
layout: mfile
title: moglBlitTexture
categories:
  - PsychOpenGL
encoding: UTF-8
---

moglBlitTexture(texid, x, y, w, h, fastblit, clamping)

moglBlitTexture blits the OpenGL texture 'texid' at offset (x,y) into the
current framebuffer. 'w x h' pixels are blitted. By default the offset is
(0,0), the size is the full size of the texture.

If you set the fastblit - flat to 1, then all other parameters are
required, all error-checking and texture engine setup is skipped and only
the minimal amount of code for initiating a blit is performed. This is
useful in inner loops of GPGPU algorithms to squeeze out more speed!

This does basically the same as [Screen](/docs/Screen)('DrawTexture') but without all the
convenience stuff contained in 'DrawTexture' - and without the possible
interference of PTB's internal drawing model. This is mostly useful for
GPGPU and image processing applications where one needs very strict
control of the way drawing is done. For everything else, use
[Screen](/docs/Screen)('DrawTexture').

Current limitation: Only rectangle textures are supported.