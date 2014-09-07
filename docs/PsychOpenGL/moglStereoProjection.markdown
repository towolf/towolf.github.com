---
layout: mfile
title: moglStereoProjection
categories:
  - PsychOpenGL
encoding: UTF-8
---

moglStereoProjection(left, top, right, bottom, near, far, zero\_plane, dist, eye)

Set up the stereo projection matrices for binocular stereo projection.
Taken verbatim from Quoc Vuong's class on Computer Graphics for Vision Research,
http://www.kyb.mpg.de/bu/people/qvuong/CGV05.html

Requires: glMatrixMode(GL.PROJECTION) being set before call. Backup your
matrices if you need'em later!



Perform the perspective projection for one eye's subfield.

The projection is in the direction of the negative z-axis.

[default: -6.0, 6.0, -4.8, 4.8]
left, right, bottom, top = the coordinate range, in the plane of zero parallax setting,
which will be displayed on the screen.

The ratio between (right-left) and (top-bottom) should equal the aspect
ratio of the display.

[default: 6.0, -6.0]
near, far = the z-coordinate values of the clipping planes.

[default: 0.0]
zero\_plane = the z-coordinate of the plane of zero parallax setting.

[default: 14.5]
dist = the distance from the center of projection to the plane of zero parallax.

[default: -0.3]
eye = half the eye separation; positive for the right eye subfield,
negative for the left eye subfield.
