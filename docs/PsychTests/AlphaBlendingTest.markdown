---
layout: mfile
title: AlphaBlendingTest
categories:
  - PsychTests
encoding: UTF-8
---

AlphaBlendingTest([screenNumber])

Perform tests of OpenGL alpha blending by drawing to the screen using
'PutImage', reading back the actual values on the [Screen](/docs/Screen) using
'GetImage' and comparing the actual values to predicted values
calcualated in MATLAB.

AlphaBlendingTest combines tests implemented separately.  You may perform
any of these tests individually, or call TestAlphaBlending to perform
them all:

AlphaBlendSettingTest -
  Test the [Screen](/docs/Screen)('BlendFunction') recalls previously stored
  alpha values.

AlphaMultiplicationTest -
  Test that alpha multiplication by values 0 and 1 ([Screen](/docs/Screen) 255) works
  with perfect precision.  OpenGL guarantees perfect precision for those
  alpha values only.

AlphaMultiplicationAccuracyTest -
  Measure the precision of alpha values between 0 and 1 ([Screen](/docs/Screen) 0 and 255) by
  drawing to the screen, then taking the difference between what was
  drawn to the screen and results of simulated blending done with
  double-precision floats.

AlphaAdditionTest -
  Test that addition of source and destination terms has perfect
  precision.