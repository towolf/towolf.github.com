---
layout: mfile
title: EyelinkGazeContingentDemo
categories:
  - GazeContingentDemos
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
Mode can have the following values:
Mode 1:
  Fovea contains original image data:
  Periphery contains grayscale-version:
Mode 2:
  Fovea contains original image data:
  Periphery contains blurred-version:
Mode 3
  Fovea contains color-inverted image data:
  Periphery contains original data:
Mode 4
  Test-case: One shouldn't see any foveated region on the
  screen - this is a basic correctness test for blending.
----

see also: EyelinkExample, EyelinkPicture