---
layout: mfile
title: PsychHelperCreateRemapCLUT
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

remapCLUTId = PsychHelperCreateRemapCLUT(cmd, arg);

Helper function for Psychtoolbox imaging pipeline, called by
PsychImaging(), not meant to be called by normal user code!

# If 'cmd' command code is zero, then:

Build a 3 rows by arg1 texels RGBA8 lookup texture for mapping of RGB
pixel values in range 0 to (arg-1) to RGBA8 framebuffer pixels. This
texture is used as CLUT texture for the
RGBMultiLUTLookupCombine\_FormattingShader.frag.txt in the image
processing chains of the imaging pipeline. If arg2 is set to 1 instead of
zero, a 32 bpc float texture is used instead of 8 bpc integer.

If 'cmd' command code is 1, then the clut texture with id arg1 is updated
with the content of clut table arg2.
