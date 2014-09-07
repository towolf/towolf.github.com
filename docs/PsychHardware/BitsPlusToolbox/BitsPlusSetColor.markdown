---
layout: mfile
title: BitsPlusSetColor
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

SetColorBitspp(windowPtr,entry,rgb)

Set the specified entry of the clut, using the Bits++ box and our
frame buffer conventions.

Prior to using this routine, Bits++ box must be in
framebuffer load mode.

This routine is not required to be speedy, and it isn't.

xx/xx/02  jmh  Wrote it, but didn't comment.
2/23/03   dhb  Added comments.
2/28/03   dhb, ptw  Add delay to make sure glitch has settled.
               Changed name, fixed up.
3/8/03    dhb  Remove call to bitsplus.