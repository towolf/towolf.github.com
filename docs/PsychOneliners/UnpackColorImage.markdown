---
layout: mfile
title: UnpackColorImage
categories:
  - PsychOneliners
encoding: UTF-8
---

[red,green,blue] = UnpackColorImage(image)

Take a color image and unpack it into three
three image planes.

Particularly useful for fixing old code
that used SCREEN('GetColorImage',....)

11/24/02  jmh, dhb  Wrote it.