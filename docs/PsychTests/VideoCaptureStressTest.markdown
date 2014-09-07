---
layout: mfile
title: VideoCaptureStressTest
categories:
  - PsychTests
encoding: UTF-8
---

Demonstrate simple use of built-in video capture engine.

VideoCaptureStressTest([fullscreen=0][, fullsize=0][, roi=[0 0 640 480]][,deviceId=0])

# Optional parameters:

'fullscreen' If set to non-zero value, the image is displayed in a
fullscreen window, as usual, otherwise a normal GUI window is used.

'fullsize' If set to 1, the cameras image is scaled up to full screen
resolution, ie. so it fills the maximum amount of display area, but
preserving the original aspect ratio.

'roi' Selects a rectangular subregion of the camera for display. By
default, it selects a [0 0 640 480] rectangle, ie. the full are of a
camera with 640 x 480 pixels resolution. This parameter may need tweaking
for some cameras, as some drivers have bugs and don't work well with all
settings.

'deviceId' Device index of video capture device. Defaults to system default.
