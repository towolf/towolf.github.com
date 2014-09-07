---
layout: mfile
title: DrawingToTextureVsOffscreenWindowTest
categories:
  - PsychTests
encoding: UTF-8
---

Draws some line into an offscreen window, displays it,
then does the same drawing into a texture.

Result should be the same, unless something is screwed wrt. texture
format, in which case one of both drawings will be flipped upside-down or
transposed etc.

This should pass on all hardware. Contributed by some unknown user
"empedia".