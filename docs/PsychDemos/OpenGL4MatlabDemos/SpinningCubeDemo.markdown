---
layout: mfile
title: SpinningCubeDemo
categories:
  - OpenGL4MatlabDemos
encoding: UTF-8
---

SpinningCubeDemo - Demonstrate use of MATLAB-OpenGL toolbox

This demo demonstrates use of OpenGL commands in a Matlab script to
perform some funky 3D animation in Psychtoolbox.
It shows a randomly spinning, textured cube. The six sides of the cube
are textured via binary texture data loaded from a file.

Stop the demo by pressing any key.

Notable implementation details:
The call InitializeMatlabOpenGL(1) at the top of the script initializes the
Matlab-OpenGL toolbox and enables the 3D gfx support in Psychtoolbox to
allow proper interfacing between the OpenGL toolbox and Psychtoolbox.

After this call, all OpenGL functions are made available to Matlab with
the same - or a very similar - calling syntax as in the C programming
language. OpenGL constants are made available in C-Style, e.g.,
GL\_DEPTH\_TEST, and in a format that is optimized for Matlab, where the
first underscore is replaced by a dot, e.g., GL.DEPTH\_TEST. The former
style is more convenient if you want to copy & paste OpenGL code written
in C into a Matlab M-File for use, but it only works if you put all your
code into one single M-File or function. The second style works in
subfunctions as well, if you place the commands "global GL" and "global
GLU" at the top of each function... This inconvenience is unavoidable due
to the design of Matlab.

In order to execute OpenGL 3D drawing commands to draw 3D stims into a
Psychtoolbox Onscreen- or offscreen window, one needs to call
[Screen](/docs/Screen)('BeginOpenGL', windowPtr). After OpenGL drawing and before
execution of standard [Screen](/docs/Screen)() commands, one needs to call
[Screen](/docs/Screen)('EndOpenGL', windowPtr) to tell Psychtoolbox that 3D drawing is
finished.

Some OpenGL functions that return complex parameters to Matlab are not
yet implemented - this is work in progress. The performance will be also
lower than when coding in a compiled language like C++ or C -- that's the
Matlab tax you'll have to pay ;-)

Apart from that, use of OpenGL for Matlab is the same as OpenGL for the C
programming language. If you are used to OpenGL coding in C, it should be
a zero effort transition to code in Matlab+PTB. If you don't know OpenGL
then get yourself one of the many good books or visit one of the many
OpenGL tutorials on the internet.

The OpenGL Red Book is a great introduction and reference for OpenGL
programming. Release 1.0 is available online, later releases can be
purchased in any good book store:

http://www.opengl.org/documentation/red\_book\_1.0/

# For more infos, code samples, tutorials, online documentation, go to:

http://www.opengl.org

The OpenGL for Matlab toolbox was developed and contributed under
GPL license by Prof. Richard F. Murray, University of York, Canada.