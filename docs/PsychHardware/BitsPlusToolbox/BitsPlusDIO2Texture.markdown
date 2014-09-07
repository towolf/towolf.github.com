---
layout: mfile
title: BitsPlusDIO2Texture
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

texturePtr = BitsPlusClut2Texture(windowPtr, mask, data, command)

  Generates a PsychToolbox texture containing the magic code and data
  required to set the DIO in Bits++ mode.

  'mask', 'data', and 'command' have the same meaning as in the function
  'bitsEncodeDIO.m'.