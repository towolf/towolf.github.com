---
layout: mfile
title: VideoCaptureToMatlabDemo
categories:
  - PsychDemos
encoding: UTF-8
---

VideoCaptureToMatlabDemo([deviceIndex])

Minimalistic demo on how to capture video data and return it in a
Matlab/Octave matrix.

The demo starts video capture on a video device, auto-detected or
specified by optional 'deviceIndex'. Instead of requesting images as
textures and displaying them in a ptb onscreen window, it requests images
as raw data in a matrix rawImage. After converting rawImage into the
standard Matlab/Octave image matrix format, it imshow()'s the image in a
standard figure window.

Press any key or wait for 600 seconds to end the demo.
