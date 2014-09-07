---
layout: mfile
title: kPsychAssumeTextureNormalized
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

rc = kPsychAssumeTextureNormalized

Returns a flag to be passed to the 'specialFlags' optional argument of
[Screen](/docs/Screen)('TransformTexture');

The flag tells the command that the input texture(s) are already in a
normalized upright format, regardless what the textures themselves claim.
This allows to save on some internal format conversion overhead if the
textures are really normalized, or if you can use some hacks in your code
to at least fake that situation.