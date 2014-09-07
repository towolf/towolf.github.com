---
layout: mfile
title: kPsychNeedHalfWidthWindow
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

rval = kPsychNeedHalfWidthWindow

Return a flag that you can pass to the 'imagingmode' parameter of
[Screen](/docs/Screen)('OpenWindow') in order to request use of half-width windows. These
onscreen windows are treated by all drawing functions (and geometry query
functions like [Screen](/docs/Screen)('Rect', window); or [Screen](/docs/Screen)('WindowSize', window);
as if they only have half the width in pixels. This is a trick to handle
dual-display stereo modes or special display modes like CRS Color++ mode
for the Bits++ box, where useable horizontal drawing area is only half
the physical monitor resolution due to the special image processing
inside the Bits++ box. Usually user scripts won't pass this flag, but
only special setup routines that are part of the Psychtoolbox itself.
