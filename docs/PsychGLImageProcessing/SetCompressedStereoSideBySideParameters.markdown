---
layout: mfile
title: SetCompressedStereoSideBySideParameters
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

SetCompressedStereoSideBySideParameters\(win, \[0, 0\], \[0.5, 1\], \[0.5, 0\], \[0.5, 1\]\);

Change parameters for over-under stereo to side-by-side stereo so that
the imaging mode will work in a display that horizontally stretches left
and right frames to fill the full res window.

This routine is called automatically by PsychImaging\(\) during onscreen
window creation with its default parameters if ...

PsychImaging\('AddTask', 'General', 'SideBySideCompressedStereo'\);

... is called during window setup.

You can call the function yourself after PsychImaging\('OpenWindow', ...\);
if you want to use non-default composition parameters for side-by-side
stereo presentation.

# This is how compressed side-by-side stereo works:

1. Usercode draws stimuli into the left-eye and righ-eye framebuffers at
   full display resolution.

2. [Screen](/docs/Screen)\('[Flip](/docs/Flip)'\) compresses those stimuli horizontally into the output
   framebuffer.

# 3. At display time, the display stretches half frames to full width        \_\_\_\_\_\_\_\_\_       \_\_\_\_\_\_\_\_\_
   | L | R |   ---\> | <-L-\>  |  +   | <-R-\>  |
   ---------        ----------      ----------

Side-by-side compressed images are one of several popular stereo HDMI
formats.

The stereo mode must have been set to 2 or 3 for this to work, or the
above mentioned PsychImaging\(\) function must have been called for setup.

# Example function call:

SetCompressedStereoSideBySideParameters\(win, \[0, 0\], \[0.5, 1\], \[0.5, 0\], \[0.5, 1\]\)

Call this function after the win = PsychImaging\('OpenWindow',...\); call
on an onscreen window in Top/Bottom stereo mode to change the parameters
of drawing the stereo views.

All parameters except the onscreen 'win'dowhandle are optional and have
reasonable builtin defaults:

'leftOffset' = Top-Left \[x,y\] offset of left eye framebuffer in relative
coordinates \[0,0\] == top-left of framebuffer, \[1,0\] == 1 display window
width to the right, \[2,0\] == 2 display window widths to the right etc.

'leftScale' = Scaling of left eye image buffer. E.g., \[1,1\] == Don't
scale. \[0.75, 0.5\] scale to 75% of original width, 50% of original
height.

'rightOffset', 'rightScale' == Ditto for right eye image.

This function was inspired and co-implemented by David Hoffman.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/SetCompressedStereoSideBySideParameters.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/SetCompressedStereoSideBySideParameters.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/SetCompressedStereoSideBySideParameters.m</code>
</div>
