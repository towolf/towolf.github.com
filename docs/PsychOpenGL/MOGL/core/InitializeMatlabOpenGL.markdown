---
layout: mfile
title: InitializeMatlabOpenGL
categories:
  - core
encoding: UTF-8
---

InitializeMatlabOpenGL([opengl\_c\_style] [, debuglevel] [, noswitchto3D] [, specialFlags=0])

InitializeMatlabOpenGL -- Initialize the OpenGL for Matlab wrapper 'mogl'.

Call this function at the beginning of your experiment script before
calling \*any\* Psychtoolbox [Screen](/docs/Screen)() command, if you intend to use low-level
OpenGL drawing commands in your script as provided by Richard Murrays
moglcore extension.

This will check if mogl is properly installed and upload all required
OpenGL constants into your Matlab workspace. It will also set up
Psychtoolbox for interfacing with external OpenGL code.

There is also a special query mode: If you set the first argument
'opengl\_c\_style' to the special value -1, then this call will do nothing
than return the old 'debuglevel', cached from a previous call to this
routine.


Options:
opengl\_c\_style = 0 / 1:
If you call InitializeMatlabOpenGL or InitializeMatlabOpenGL(0), all
constants will be loaded in structs in order to avoid cluttering the
Matlab workspace too much. You'll have to replace all GL\_xxx calls by
GL.xxx calls, e.g., GL\_LIGHTING becomes GL.LIGHTING .
If you call InitializeMatlabOpenGL(1), then all constants will additionally
be provided in standard C-Style syntax, aka GL\_LIGHTING.

debuglevel = 0 to 3: Setting debuglevel == 0 will disable debug-output.
A level of 1 will cause MOGL to output error messages and abort your
scripts execution if it detects any OpenGL error. A level of 2 provides
additional information that may help you to optimize your code. level 3
means to be very verbose.

noswitchto3D: Setting this optional parameter to 1 will only load the GL
constants and moglcore, but it won't switch PTB itself into 3D mode. This
is useful if your code needs access to OpenGL for some configuration work
but doesn't intend to do real 3D rendering. Mostly called from PTB
internal helper functions, e.g., imaging pipeline. Defaults to zero, aka
"switch to real 3D mode".

specialFlags = 0: Setting this optional parameter will enable some
special properties of the created OpenGL context. You can add the
following values to setup such a special configuration:

   \+ 2  == Enable and attach an OpenGL accumulation buffer, with
   requested 16 bits resolution per color component, i.e., R16G16B16A16.
   The system may decide to allocate an accumulation buffer with more or
   less than the preferred 16 bpc, or it may decide not to allocate an
   accumulation buffer at all. On most graphics cards the accumulation
   buffer is implemented in software - using it may drastically reduce
   graphics performance down to redraw rates of only a few frames per
   second! There are better methods based on clever use of alpha blending
   and floating point resolution offscreen windows on modern graphics
   cards, or by direct low-level use of framebuffer objects.

   -\> This flag is needed to make the glAccum() command work.



The initial OS/X PowerPC version of the 'OpenGL for Matlab' low level
interface wrapper mogl was developed, implemented and generously
contributed to Psychtoolbox under the GPL license by Prof. Richard F.
Murray, University of York, Canada. Porting to other operating systems
and architectures, OpenGL 2.x support, and further extensions and
maintenance has been done by Mario Kleiner.

The code has been relicensed by Richard Murray and Mario Kleiner to the
more permissive MIT license since 2011.
