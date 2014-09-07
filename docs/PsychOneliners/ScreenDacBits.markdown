---
layout: mfile
title: ScreenDacBits
categories:
  - PsychOneliners
encoding: UTF-8
---

dacBits = ScreenDacBits(windowPtrOrScreenNumber)

What is the precision of the DACs on this graphics card?

At present you need to know the bit depth of your graphics board's DAC
to determine how to write its CLUT, i.e. [Screen](/docs/Screen) 'SetClut' or 'Gamma'.
Use this routine and ScreenUsesHighGammaBits, instead of the the brand-
and platform-specific IsRadiusThunder10 and IsATIRadeon10, to keep your
program as general as possible, not tied to particular hardware or
platform.

The value is set in PrepareScreen.m.

See also LoadClut, ScreenPixelSize, ScreenUsesHighGammaBits, ScreenClutSize.