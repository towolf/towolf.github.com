---
layout: mfile
title: Create2DGaussianBlurShader
categories:
  - PsychGLSLShaders
encoding: UTF-8
---

blurshader = Create2DGaussianBlurShader(stddev, width)
EXPERIMENTAL - THIS FEATURE IS IN BETA-STAGE AND MAY CHANGE
IN THE FUTURE OR NOT WORK AT ALL IN THE PRESENT!

Create a GLSL shader which uses a 2D gaussian filter kernel to
apply gaussian blur onto a texture. Returns the handle 'blurshader',
which can be used via glUseProgram(blurshader) to activate the shader.

stddev = Standard deviation of kernel to use. Defaults to 2.5.
width  = Width of filter-kernel. Currently only a width of 5 is
supported, so this argument is optional and defaults to 5.

Currently you will need the Matlab imageprocessing toolbox for this to
work, as we use the toolbox function 'fspecial' to compute the filter
kernel.

# Example of use:

Somewhere during initialization of your script you call:
blurshader = Create2DGaussianBlurShader(2.5);

# When you want to draw an image blurred with a gaussian lowpass, you do:

glUseProgram(blurshader);
[Screen](/docs/Screen)('DrawTexture', win, mytexture, ....);
glUseProgram(0);
