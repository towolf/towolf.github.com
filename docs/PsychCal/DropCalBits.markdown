---
layout: mfile
title: DropCalBits
categories:
  - PsychCal
encoding: UTF-8
---

cal = DropCalBits(cal,whichScreen,[forceBit])

Drops the bitdepth of a calibration file if
necessary.  Useful for running programs
transparently on 8 and 10 bit hardware.

If arg forceBits is passed, it is used as
the current hardware depth.  Otherwise the
reported DACBits of whichScreen is used.

This code assumes calibration was done at
equally spaced levels in RGB settings, as is
the case with our calibration routines.  May
not generalize, and I haven't worried about
the roundoff errors.  Certainly OK for basic
use.

2/13/05     dhb     Wrote it.