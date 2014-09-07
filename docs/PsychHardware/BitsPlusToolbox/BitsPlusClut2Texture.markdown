---
layout: mfile
title: BitsPlusClut2Texture
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

texturePtr = BitsPlusClut2Texture(windowPtr, clut)

  Generates a PsychToolbox texture containing the CLUT + magic code
  required to set the clut in Bits++ mode.

  'clut' should be a 256x3 matrix consisting of values in the range
  specified by [Screen](/docs/Screen)('ColorRange'), which is by default [0, 255].