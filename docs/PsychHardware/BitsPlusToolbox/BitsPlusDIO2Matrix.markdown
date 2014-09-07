---
layout: mfile
title: BitsPlusDIO2Matrix
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

encodedDIOdata = BitsPlusDIO2Matrix(mask, data, command);

Generates a Matlab matrix containing the magic code and data
required to set the DIO port of CRS Bits++ box in Bits++ mode.

'mask', 'data', and 'command' have the same meaning as in the function
'bitsEncodeDIO.m'.

This is a helper function, called by bitsEncodeDIO and
BitsPlusDIO2Texture, as well as from BitsPlusPlus when used with the
imaging pipeline. It takes parameters for controlling Bits++ DIO and
generates the data matrix for the corresponding T-Lock control code. This
matrix is then used by the respective calling routines to convert it into
a texture, a framebuffer image, or whatever is appropriate.

This is just to unify the actual T-Lock encoding process in one file, so
we don't have to edit or fix multiple files if something changes...
