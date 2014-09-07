---
layout: mfile
title: CreateDisplayWarp
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

\[warpstruct, filterMode\] = CreateDisplayWarp\(window, calibfilename \[, showCalibOutput=0\]\);

Helper routine for Geometric display undistortion mapping, not to be
called inside normal PTB scripts\!

This function reads a display calibration file 'calibfilename' and builds
a "geometric warp function" based on the calibration information in
'calibfilename' for the onscreen window with handle 'window'. It returns
a struct 'warpstruct' that defines the created warp function. You could
pass this 'warpstruct' as a parameter to the Psychtoolbox command...

PsychImaging\('AddTask', viewchannel, 'GeometryCorrection', warpstruct\);

However, you normally do not call this routine directly from your script. Its
called internally by the PsychImaging\(\) command...

PsychImaging\('AddTask', viewchannel, 'GeometryCorrection', calibfilename\);

...in order to setup PTB's imaging pipeline for realtime geometry
correction, based on the calibration info in the file 'calibfilename'.

Example: You created a calibration file 'mycalib.mat' to undistort the
left view display of a stereo setup. Then you could apply this
undistortion function via the following setup code:

PsychImaging\('PrepareConfiguration'\);
PsychImaging\('AddTask', 'LeftView', 'GeometryCorrection', 'mycalib.mat'\);
window = PsychImaging\('OpenWindow', screenid\);

This would open an onscreen window just as window=[Screen](/docs/Screen)\('OpenWindow', screenid\);
would do. It would configure the window for automatic undistortion based
on the data in 'mycalib.mat'.

Psychtoolbox provides multiple different interactive setup routines that
allow you to create a calibration file for your setup. Currently the
following routines are provided:

DisplayUndistortionBVL.m    -- Undistortion based on 3rd order polynomial
surface. This is the recommended calibration procedure for most cases -
Proven in real-world use on many different display types.

DisplayUndistortionBezier.m -- Undistortion based on a NURBS surface \(Non
uniform rational bezier spline surface\). A simple procedure.

DisplayUndistortionHalfCylinder.m -- Undistortion for projection of
images to a half-cylindrical projection surface.

DisplayUndistortionSphere.m -- Undistortion for projection of
images to a spherical or half-spherical projection surface.

DisplayUndistortionCSV.m -- Import undistortion information from
a .csv file with a warp mesh description suitable for use with NVidia's
Warp API. This creates a compatible display warping to use of that NVidia
technology.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/CreateDisplayWarp.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/CreateDisplayWarp.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/CreateDisplayWarp.m</code>
</div>
