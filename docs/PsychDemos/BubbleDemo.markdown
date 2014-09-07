---
layout: mfile
title: BubbleDemo
categories:
  - PsychDemos
encoding: UTF-8
---

BubbleDemo(mode, ms, myimgfile)

# OS X and WINDOWS

Demo implementation of a generic bubble display.
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


see also: PsychDemos, MovieDemo, DriftDemo