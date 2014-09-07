---
layout: mfile
title: MakeTextureTimingTest
categories:
  - PsychTests
encoding: UTF-8
---

MakeTextureTimingTest

[Screen](/docs/Screen) 'MakeTexture' both allocates memory to hold an OpenGL texture and
loads a MATLAB matrix into the OpenGL texture. TestMakeTextureTiming
times those two steps separately, reporting the fraction of time which
MakeTexture spends allocating memory.

On 1GHz G4, MakeTexture spends less than 3% of its time allocating memory.
Providing separate [Screen](/docs/Screen) subfuntions to allocate and fill textures would
gain little.

see also: PsychTests


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychTests/MakeTextureTimingTest.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychTests/MakeTextureTimingTest.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychTests/MakeTextureTimingTest.m</code>
</div>
