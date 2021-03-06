---
layout: mfile
title: VideoRefreshFromMeasurement
categories:
  - PsychBasic
encoding: UTF-8
---

ifi = VideoRefreshFromMeasurement(window [, samples=600]);

Measure video refresh interval for onscreen windows display with a method
that is supposed to be as robust and accurate as possible.

'window' is the onscreen window handle for the window whose corresponding
display should be measured.

'samples' is the (optional) number of refresh samples to take into
account.

This routine returns the estimated refresh duration in seconds. It uses
one of multiple calibration strategies, preferring more accurate ones but
falling back to less accurate ones if the accurate ones are not supported
by your system:

1\. On MacOS/X it tries to use low-level VBL interrupt timestamps.
2\. If that fails it tries to get the measurement from the beamposition
   measurement method.
3\. If that fails it returns the measurment from
   [Screen](/docs/Screen)('GetFlipInterval').
