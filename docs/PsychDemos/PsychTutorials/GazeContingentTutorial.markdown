---
layout: mfile
title: GazeContingentTutorial
categories:
  - PsychTutorials
encoding: UTF-8
---

----

Demo implementation of a generic gaze-contingent display.
We take one input image and create - via image processing - two images
out of it: An image to show at the screen location were the subject
fixates (According to the eye-tracker). A second image to show in the
peripery of the subjects field of view. These two images are blended into
each other via a gaussian weight mask (an aperture). The mask is centered
at the center of gaze and allows for a smooth transition between the two
images.

This illustrates an application of OpenGL Alpha blending by compositing
two images based on a spatial gaussian weight mask. Compositing is done
by the graphics hardware.

See also: PsychDemos, MovieDemo, DriftDemo