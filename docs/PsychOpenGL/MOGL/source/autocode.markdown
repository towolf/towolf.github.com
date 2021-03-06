---
layout: mfile
title: autocode
categories:
  - source
encoding: UTF-8
---

AUTOCODE.M  Generate MATLAB-OpenGL or OpenAL interface code from OpenGL or OpenAL header files

Usage: autocode(overwrite, glheaderpath, openal).
glheaderpath is the path to the OpenGL gl.h and glu.h header files.
It defaults to /System/Library/Frameworks/OpenGL.framework/Headers/

If overwrite is == 1, then existing M-Files are overwritten, else (and
this is the default) existing files are not touched.

If openal is == 1, then OpenAL code is generated, instead of OpenGL code.

18-Dec-05 -- created (RFM)
05-Mar-06 -- added option to spec. glheaderpath (MK)
30-May-06 -- added option 'overwrite' to not overwrite M-Files. (MK)
             added additional parsing code for headers/glext\_edit.h
06-Feb-07 -- added support for OpenAL (MK)
24-Mar-11 -- Silence mlint warnings. (MK)
01-Apr-12 -- Adapt to parsing of current glext\_edit.h from OpenGL registry. (MK)