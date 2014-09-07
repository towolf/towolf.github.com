---
layout: mfile
title: DisplayUndistortionCSV
categories:
  - PsychGLImageProcessing
---

scal = DisplayUndistortionCSV\(calibinfilename \[, caliboutfilename\]\[, screenid\]\)

Geometric display calibration procedure for undistortion of distorted
displays. Needs graphics hardware with basic support for the PTB imaging
pipeline \(see below\).

Many display devices, e.g., video beamers and most CRT displays cause
some amount of spatial distortion to your visual stimuli during display.
Video projection onto curved screens will cause an especially large
amount of distortion.

Psychtoolbox can "undistort" your visual stimuli for you: At stimulus
onset time, PTB applies a geometric warping transformation to your
stimulus which is meant to counteract or cancel out the geometric
distortion caused by your display device. If both, PTB's warp transform
and the implicit distortion transform of the display match, your stimulus
will show up undistorted on the display device.

# For this to work, PTB needs two things:

1. Recent graphics hardware with support for the PTB imaging pipeline:
See our Wiki for recommendations. However, all ATI cards starting with
Radeon 9500 and all NVidia cards of type GeForce\-FX5200 and later, as
well as the Intel\-GMA 950 and later should be able to do it, although
more recent cards will have a higher performance.

2. A calibration file that defines the warp transformation to apply. Your
experiment script will load that file into [Screen](/docs/Screen)'s "warp engine" at the
beginning of your experiment and [Screen](/docs/Screen)\(\) will automatically apply that
warping to each stimulus image before output.

DisplayUndistortionCSV defines a continous mapping \(x', y'\) = f\(x, y\)
from uncorrected input pixel locations \(x,y\) in your stimulus image to
output locations \(x', y'\) on your display. This mapping is defined by a
linear mesh of quadrilaterals, as read from the given input file. The
file format is compatible with the Warp\-API of NVidia's proprietary
graphics drivers for some high\-end Quadro GPUs on Windows\-7 and later.


How to use:
\-\-\-\-\-\-\-\-\-\-\-


# Execute the function with the following parameters:


`calibinfilename` is the path and filename of an existing calibration
file. This must be a ASCII file with a one\-line header, describing the
meaning of the data columns, followed by at least 4 lines with numeric
calibration data. Each line defines a data row, which has six columns,
delimited with a semicolon ';'. The columns of a row have the following
meaning: vx;vy;tx;ty;c;r

vx = Output mesh vertex x position.
vy = Output mesh vertex y position.
tx = Input framebuffer corresponding x position.
ty = Input framebuffer corresponding y position.
c  = Column index of the vertex.
r  = Row index of the vertex.

Each row describes one vertex of a mesh of connected quadrilaterals
\(GL\_QUADS\). The mesh is basically a rectilinear grid, whose "grid line"
intersections are the locations of the vertices. The mesh gets distorted
by moving around those intersections, thereby forming the actual warp
mesh.

Pixel color values at location \(tx,ty\) of the input framebuffer are
projected to location \(vx,vy\) of the warped output framebuffer. Quads are
defined by 4 vertices which define their corners. Pixel sampling and
output locations inside quads are bilinearly interpolated for a smooth
warp grid. The origin of the calibration coordinate system is the
top\-left framebuffer / screen corner \(0,0\), x\-axis points to the right,
y\-axis points downwards. All coordinates are normalized to a unit square
screen. The range 0.0 \- 1.0 maps to the screen width or height \(0.0 =
Left or Top, 1.0 = Right or bottom\) and is subject to rescaling for a
specific displays real resolution. Values outside the 0\-1 range are
allowed. The corresponding mesh locations will be clipped to screen
corners during warping.

The file format described here is the format expected by NVidia's
Warp\-API, as implemented in some binary NVidia graphics drivers for some
high\-end Quadro graphics cards on Windows\-7 and later. This allows to
reuse the file for both NVidia proprietary distortion correction and for
Psychtoolbox.


`caliboutfilename` Name of the file to which calibration results should
be stored. If no name is provided, the file will be stored inside the
'GeometryCalibration' subfolder of your psychtoolbox configuration
directory \(path is PsychToolboxConfigDir\('GeometryCalibration'\). The
filename will contain the screenid of the display that was calibrated.


`screenid` screen id of the target display for calibration. The parameter
is optional, defaults to zero, and is only used to generate the default
filename for the output file.


This script will print out a little snippet of code that you can paste
and include into your experiment script \- That will automatically load
the calibration result file and apply the proper undistortion operation.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/DisplayUndistortionCSV.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/DisplayUndistortionCSV.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/DisplayUndistortionCSV.m</code>
</div>
