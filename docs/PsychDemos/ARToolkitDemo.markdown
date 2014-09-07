---
layout: mfile
title: ARToolkitDemo
categories:
  - PsychDemos
encoding: UTF-8
---

Use ARToolkit to track and visualize 3D objects in live-video.

Usage: ARToolkitDemo([multiMarker = 2])

Minimalistic demo on how to capture video data and use ARToolkit to
detect and track the rigid position and orientation of markers, then
visualize corresponding 3D objects on top of video via OpenGL.

Please note that ARToolkit is only supported when running Psychtoolbox
under GNU/Octave, not when using it with Matlab. Therefore this demo
won't work with Matlab.

# Parameters:

multiMarker = If set to 2 (default), track single markers. If set to 1,
track so called multi markers or composite markers for more robustness
against occlusion of single markers. A setting of 3 (=1+2) should track
both types of markers simultaneously, but this doesn't seem to work well
yet.
