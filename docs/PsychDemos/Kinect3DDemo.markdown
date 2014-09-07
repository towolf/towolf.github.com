---
layout: mfile
title: Kinect3DDemo
categories:
  - PsychDemos
encoding: UTF-8
---

Kinect3DDemo - Capture and display video and depths data from a Kinect box.

# Usage:

Kinect3DDemo([stereomode=0])

This connects to a Microsoft Kinect device on the USB bus, then captures
and displays video and depths data delivered by the Kinect.

This is an early prototype.

# Control keys and their meaning:

'a' == Zoom out by moving object away from viewer.
'z' == Zoom in by moving object close to viewer.
Left- and Right cursor keys == Rotate object around vertical axis.
Up- and Down cursor keys == Rotate object around horizontal axis.
SPACE = Toggle live 3D feed.
'm' = Toggle mesh display vs. point-cloud display.
ESCAPE == Quit demo.

# Options:

stereomode = n. For n \> 0 this activates stereoscopic rendering - The shape is
rendered from two slightly different viewpoints and one of Psychtoolbox's
built-in stereo display algorithms is used to present the 3D stimulus. This
is very preliminary so it doesn't work that well yet.

See help PsychKinect, help PsychKinectCore and help InstallKinect for
further info.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/Kinect3DDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/Kinect3DDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/Kinect3DDemo.m</code>
</div>
