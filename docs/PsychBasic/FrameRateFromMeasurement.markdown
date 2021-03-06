---
layout: mfile
title: FrameRateFromMeasurement
categories:
  - PsychBasic
encoding: UTF-8
---

ifi = VideoRefreshFromMeasurement(window, samples)

This function should determine the exact duration of the displays video
refresh interval with the highest possible precision, using whatever
method proves to be the most accurate on your system.

You must provide 'window' the handle to the onscreen window whose
associated display you want to be measured and (optionally) 'samples',
the number of samples to take for computation of video refresh interval.

The function returns the measured interval in units of seconds.

CAUTION: This is unfinished alpha quality code. While it works well on
some system setups, it doesn't yet on others and will need more
fine-tuning in the future. For most purpose, the values returned by
[Screen](/docs/Screen)('GetFlipInterval', window); are perfectly useable and the
recommended way of getting the video refresh duration.