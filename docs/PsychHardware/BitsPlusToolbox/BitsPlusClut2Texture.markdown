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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/BitsPlusToolbox/BitsPlusClut2Texture.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/BitsPlusToolbox/BitsPlusClut2Texture.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/BitsPlusToolbox/BitsPlusClut2Texture.m</code>
</div>
