---
layout: mfile
title: SetStereoSideBySideParameters
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

Change parameters for side-by-side stereo display modes (4 and 5).

SetStereoSideBySideParameters(win [, leftOffset][, leftScale][, rightOffset][, rightScale])

Call this function after the win = PsychImaging('OpenWindow',...); call on an
onscreen window in side-by-side stereo mode to change the parameters
of drawing the stereo views.

All parameters except the onscreen 'win'dowhandle are optional and have
reasonable builtin defaults:

'leftOffset' = Top-Left [x,y] offset of left eye framebuffer in relative
coordinates [0,0] == top-left of framebuffer, [1,0] == 1 stereo window
width to the right, [2,0] == 2 stereo window width to the right etc.

'leftScale' = Scaling of left eye image buffer. E.g., [1,1] == Don't
scale. [0.75, 0.5] scale to 75% of original width, 50% of original
height.

'rightOffset', 'rightScale' == Ditto for right eye image.
