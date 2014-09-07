---
layout: mfile
title: PolarToSensor
categories:
  - PsychCal
encoding: UTF-8
---

[sensor] = PolarToSensor(pol)

Converts from polar sensor coordinates to
rectangular sensor coordinates.

Polar coordinates are defined as radius, azimuth, and elevation.

Inverts SensorToPolar.

See also SensorToPolar, SensorToCyl, CylToSensor.

9/26/93    dhb   Added calData argument.
2/6/94     jms   Changed 'polar' to 'pol'
2/20/94    jms   Added single argument case to avoid cData.
4/5/02     dhb, ly  New calling interface.
11/6/06    dhb   Only allow one input arguemnt.