---
layout: mfile
title: BitsPlusSetClut
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

 BitsPlusSetClut(windowPtr, clutOrTexturePtr, [rect], [doFlip])

Prior to using this routine, Bits++ box must be in
framebuffer load mode.

'clutOrTexturePtr' will either be a 256x3 matrix in the range [0,2^16-1]
or it will be a texture generated by BitsPlusPlusClut2Texture.

'rect' lets you define the rect that specifies where the magic code is
written.  For a typical application, this should be left empty.  However,
for programs that modify the projection matrix via MOGL, you will want to
change this to draw the magic code in a more cosmetically appealing
location.

If 'doFlip' is set to 1, then BitsPlusSetClut will call flip at the
end of the function.  By default, this value is 1.