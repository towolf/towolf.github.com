---
layout: mfile
title: SensorToPrimary
categories:
  - PsychCal
encoding: UTF-8
---

[primary] = SensorToPrimary(cal,sensor)

Convert from sensor color space coordinates to primary
coordinates.

This depends on the standard calibration globals.

9/26/93    dhb   Added calData argument.
10/19/93   dhb   Allow device characterization dimensions to exceed
                 linear settings dimensions.
11/11/93   dhb   Update for new calData routines.
11/17/93   dhb   Newer calData routines.
8/4/96     dhb   Update for stuff bag routines.
8/21/97    dhb   Update for structures.
4/5/02     dhb, ly  New calling convention.  Internal naming not changed fully.