---
layout: mfile
title: SimpleHDRDemo
categories:
  - BrightSideDisplay
encoding: UTF-8
---

SimpleHDRDemo([imfilename][, dummymode][, sf]) -- Load and show a high dynamic range image
on the BrightSide Technologies High Dynamic Range display device.

'imfilename' - Filename of the HDR image to load. Will load our standard
low-dynamic range 'konijntjes' if 'imfilename' is omitted.

'dummymode' - If set to 1 we only run in emulation mode without use of
the HDR device or BrightSide core library.

'sf' - Scaling factor to apply.

Btw. you can find lot's of nice free HDR images by Googling on the
internet!

Except for buying and installing the display device and control
libraries, usage with Psychtoolbox is pretty straightforward. Modify your
scripts in the following manner:

1\. Use BrightSideHDR('OpenWindow', ...) instead of [Screen](/docs/Screen)('OpenWindow',
...) -- Will perform all additional display setup work for you.

2\. Use HDRRead(imfilename) instead of imread(imfilename) to load HDR
image files as Matlab matrices.

3\. Set the 'floatprecision' flag of [Screen](/docs/Screen)('MakeTexture', ...) to 1 or 2
to enforce creation of HDR textures from your image matrix.

4\. Optionally you can use the [Screen](/docs/Screen)('ColorRange', ...) command to
upscale or downscale color values for normal 2D drawing commands. This
won't affect drawing of textures.

5\. Optionally you can use fragment shaders to perform on-the-fly image
processing when drawing an image, e.g., gamma correction, scaling, color
conversion, tone-mapping. See the more advanced demos on how to do this.

History:
Written 2006 by Mario Kleiner - MPI for Biological Cybernetics, Tuebingen, Germany
and Oguz Ahmet Akyuz - Department of Computer Science, University of Central Florida.