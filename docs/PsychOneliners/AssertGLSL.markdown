---
layout: mfile
title: AssertGLSL
categories:
  - PsychOneliners
encoding: UTF-8
---

AssertGLSL

Break and issue an error message if the given combination of graphics
hardware and graphics hardware driver does not support the OpenGL Shading
Language (GLSL). This command needs to be executed after opening an
onscreen window, because it needs a valid OpenGL context to work.

# HISTORY
3/29/06   mk     wrote it.
6/12/12   dn     findstr is deprecated, changed to strfind