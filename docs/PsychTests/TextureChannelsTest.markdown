---
layout: mfile
title: TextureChannelsTest
categories:
  - PsychTests
encoding: UTF-8
---

TextureChannelsTest

Test proper assignment of matrix layers to RGBA texture channels.

# What you should see during the test:

1\. A red square on a black background. Keypress!
2\. A green square on a black background. Keypress!
3\. A blue square on a black background. Keypress!
4\. A black screen. Keypress!
End.

If you see different colors in different order, then
something in the RGBA path of [Screen](/docs/Screen)('MakeTexture') is
broken, e.g., due to some machine endian issue.
