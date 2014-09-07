---
layout: mfile
title: VideoDVCamCaptureDemo
categories:
  - PsychDemos
encoding: UTF-8
---

Demonstrate simple use of built-in video capture engine with DV consumer cameras.

VideoDVCamCaptureDemo\(\[fullscreen=0\]\[, fullsize=0\]\[, roi\]\[, depth\]\[,deviceId=0\]\[, moviename\]\)

VideoDVCamCaptureDemo initializes the first attached and supported DV firewire
consumer camera, then shows its video image in a Psychtoolbox window.
A press of the ESCape key ends the demo.

# Optional parameters:

'fullscreen' If set to non-zero value, the image is displayed in a
fullscreen window, as usual, otherwise a normal GUI window is used.

'fullsize' If set to 1, the cameras image is scaled up to full screen
resolution, ie. so it fills the maximum amount of display area, but
preserving the original aspect ratio.

'roi' Set to \[0 0 720 576\] for a PAL-DV camera and \[0 0 720 480\] for a NTSC-DV camera.
Default is PAL if omitted.

'deviceId' Device index of video capture device. Defaults to system default. You can
also specify a gst-launch style string to define a videosource here. Or you can set
the special string deviceId = 'X' so builtin spec strings suitable for each operating
system will be used.

'moviename' Name string for selection of filename of a target movie file to
which video should be recorded. Defaults to none,ie., no video recording.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/VideoDVCamCaptureDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/VideoDVCamCaptureDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/VideoDVCamCaptureDemo.m</code>
</div>
