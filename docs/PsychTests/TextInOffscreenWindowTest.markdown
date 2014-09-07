---
layout: mfile
title: TextInOffscreenWindowTest
categories:
  - PsychTests
encoding: UTF-8
---

TextInOffscreenWindowTest

Compare text drawn into an offscreen window to text drawn into an
onscreen window.

[Screen](/docs/Screen) currently fails this test; [Screen](/docs/Screen)('DrawText') draws slightly
differently into onscreen and offscreen windows. Visual examination of
the difference between onscreen and offscreen text shows that the
onscreen texts is larger by about two pixels.

Until this is resolved, we recommend not mixing onscreen and offscreen
text rendering if you require exact matching between text.

We don't yet know why this fails. The problem seems to have to do with
differences between how textures are rendered into onscreen and offscreen
windows.  That could be either because of a bug in [Screen](/docs/Screen), or because the
OpenGL software renderer used for offscreen windows rasterizes textures
slightly differently than the  hardware renderer used for onscreen
windows. We don't yet have a way to compare textures in onscreen and
offscreen windows indepently of drawing text because 'DrawTexture' still
uses OpenGL extensions not provided in offscreen contexts.
