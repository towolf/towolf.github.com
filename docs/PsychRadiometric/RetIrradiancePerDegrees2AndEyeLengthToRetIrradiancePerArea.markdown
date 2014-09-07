---
layout: mfile
title: RetIrradiancePerDegrees2AndEyeLengthToRetIrradiancePerArea
categories:
  - PsychRadiometric
encoding: UTF-8
---

retIrradiance\_PerArea = RetIrradiancePerDegrees2AndEyeLengthToRetIrradiancePerArea(retIrradiance\_PerDegrees2,eyeLength)

Convert retinal irradiance measured in units of Y/deg^2 to units of
Y/x^2, where x is a unit of distance (m, cm, mm, um, etc.) and
Y is a measure of light amount (Watts, Joules, quanta/sec, quanta, etc.)

Eye length should be passed in units of x.

The conversion assumes that we are in the small angle regime, where
degrees are essentially linear with retinal extent.

See also: PsychRadiometric, RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2.

6/23/13  dhb  Wrote it.