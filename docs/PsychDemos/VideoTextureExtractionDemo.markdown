---
layout: mfile
title: VideoTextureExtractionDemo
categories:
  - PsychDemos
encoding: UTF-8
---

Use ARToolkit to track and visualize 3D objects in live-video.

Usage: ARToolkitDemo([lightson = 0][, objtype = 3][, multiMarker = 2])

Minimalistic demo on how to capture video data and use ARToolkit to
detect and track the rigid position and orientation of markers, then
visualize corresponding 3D objects on top of video via OpenGL.

# Parameters:

multiMarker = If set to 2 (default), track single markers. If set to 1,
track so called multi markers or composite markers for more robustness
against occlusion of single markers. A setting of 3 (=1+2) should track
both types of markers simultaneously, but this doesn't seem to work well
yet.
