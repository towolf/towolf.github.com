---
layout: mfile
title: SensorToPolar
categories:
  - PsychCal
encoding: UTF-8
---

 [pol] = SensorToPolar(sensor)

 Converts from sensor rectangular coordinates to polar
 coordinates.

 Polar coordinates are defined as radius, azimuth, and elevation.

 See also PolarToSensor, SensorToCyl, CylToSensor.

 9/9/93 jms It didn't work for matrix inputs, because a
                matrix '^' needed to be a by-element '.^'
 9/26/93 dhb   Added calData argument.
 2/6/94  jms   Changed 'polar' to 'pol'
 2/20/94 jms   Added single argument case to avoid cData
 4/6/96  dhb    Fixed bug noted by ccc.  Need to use four quadrant
                arctangent atan2().
 5/20/98 dhb   Fix little bug, make sure index is not empty.
 4/5/02  dhb, ly  New calling interface.
 11/6/06 dhb   Only allow one input argument.
 2/10/07 dhb   Finish above fix.