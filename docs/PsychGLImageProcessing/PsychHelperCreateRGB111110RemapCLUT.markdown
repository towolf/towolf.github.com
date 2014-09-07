---
layout: mfile
title: PsychHelperCreateRGB111110RemapCLUT
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

remapCLUTId = PsychHelperCreateRGB111110RemapCLUT;

Helper function for Psychtoolbox imaging pipeline, called by
PsychImaging(), not meant to be called by normal user code!

Build a 3 rows by 2048 texels RGBA8 lookup texture for mapping HDR RGB
pixel values in range 0-2047 (ie. 11 bpc resolution) to RGBA8 framebuffer
pixels which will be suitable to drive a RGB11-11-10 framebuffer scanout
engine (CRTC). If a graphics cards framebuffer scanout engine CRTC is
configured for 11-11-10 ~ 11 bpc framebuffer mode, this will make sure that
HDR pixel data is shown properly onscreen.

This texture is used as CLUT texture for the
RGBMultiLUTLookupCombine\_FormattingShader.frag.txt in the final output
formatting chain of the imaging pipeline.

The expected pixel layout in 11bpc mode is: RGB111110, ie.:
R11G11B10 -- That's how a 32 bit pixel is interpreted for video
scanout. However the OpenGL system on all current OS with standard
drivers can only output A8R8G8B8 formatted pixels. We solve this via the
imaging pipeline: [Screen](/docs/Screen)() and OpenGL drawing ops go to the imaging
pipelines virtual framebuffer with 16bpc float or 32 bpc float precision.
At [Flip](/docs/Flip) time, our shader remaps that 0.0 - 1.0 values to the range 0-2047
ie. approx. 11 bpc, then uses the CLUT texture created with this function to
lookup corresponding ARGB8 color tuples for the framebuffer, combines
them into a single ARGB8 tuple by addition (logical OR), then writes that
ARGB tuple to the framebuffer. At display scanout time, the CRTC's will
find 32 bit pixels properly formatted for RGB111110 scanout.

History:
\8-June-2014  Written - Derived from PsychHelperCreateARGB2101010RemapCLUT.m (MK).


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/PsychHelperCreateRGB111110RemapCLUT.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/PsychHelperCreateRGB111110RemapCLUT.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/PsychHelperCreateRGB111110RemapCLUT.m</code>
</div>
