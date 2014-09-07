---
layout: mfile
title: SetStereoBlueLineSyncParameters
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

Change parameters for drawing of frame-sequential stereo blue line sync lines for shutter glasses (stereo goggles).

SetStereoBlueLineSyncParameters(win [, vPos=max][, hFraction=0.25][, lineColor=[1,1,1]])

Call this function after the win = [Screen](/docs/Screen)('OpenWindow',...); call on an
onscreen window in frame-sequential stereo mode to change the parameters
of drawing of stereo sync lines, as needed by stereo goggles or shutter
glasses like, e.g., CrystalEyes glasses. Enable automatic sync lines if
they aren't enabled already. Sync lines are auto-enabled on OS/X.

All parameters except the onscreen 'win'dowhandle are optional and have
reasonable builtin defaults:

'vPos': Vertical position of the sync line: Default to windowheight - 1.

'hFraction': Sync lines for left eye view are drawn starting on the left
border with a length of hFraction \* windowWidth. Right eye lines are
drawn with a length of (1-hFraction) \* windowWidth.

The default of 0.25 should be ok for at least CrystalEyes goggles

'lineColor' intensity of the color channels for drawing the line in range
zero to one: Default is [1,1,1] = max red, green and blue --> A white
sync line. A setting of [0,0,1] = red off, green off, blue max would
create a classic blue sync line. However, some CrystalEyes stereoenablers
had problems detecting the signal this way, so we default to all-white.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/SetStereoBlueLineSyncParameters.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/SetStereoBlueLineSyncParameters.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/SetStereoBlueLineSyncParameters.m</code>
</div>
