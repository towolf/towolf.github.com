---
layout: mfile
title: RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2
categories:
  - PsychRadiometric
encoding: UTF-8
---

retIrradiance\_PerDegrees2 = RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2(retIrradiance\_PerArea,eyeLength)

Convert retinal irradiance measured in units of Y/x^2 to units of
Y/deg^2, where x is a unit of distance (m, cm, mm, um, etc.) and
Y is a measure of light amount (Watts, Joules, quanta/sec, quanta, etc.)

Eye length should be passed in units of x.

The conversion assumes that we are in the small angle regime, where
degrees are essentially linear with retinal extent.

See also: PsychRadiometric, RetIrradiancePerDegrees2AndEyeLengthToRetIrradiancePerArea.

6/23/13  dhb  Wrote it.