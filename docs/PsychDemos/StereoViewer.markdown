---
layout: mfile
title: StereoViewer
categories:
  - PsychDemos
encoding: UTF-8
---

StereoViewer(leftimfile, rightimfile [,stereoMode=8] [,imaging=0])

Minimalistic viewer for stereo image pairs. Reads image for left-eye from
file 'leftimfile', reads right-eye image from file 'rightimfile'.
'stereoMode' mode of presentation, defaults to mode 8 (Red-Blue
Anaglyph). 'imaging' if set to 1, will use the Psychtoolbox imaging
pipeline for stereo display -- allows to set gains for anaglyph stereo.

The viewer just shows the image pair. The left image is centered on the
screen, the right images position can be moved by moving the mouse cursor
to align for inter-eye distance. Press any key to quit the viewer.