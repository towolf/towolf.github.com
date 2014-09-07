---
layout: mfile
title: MapIndexColorThroughClut
categories:
  - PsychOneliners
encoding: UTF-8
---

framebufferTrue = MapIndexColorThroughClut(framebufferIndex,clut)

Take an index color frame buffer and a clut, produce a true color
framebuffer.  This is based on integers, not the [0-1] clut model of
OpenGL and PTB-3.

3/22/05     dhb     Wrote it.