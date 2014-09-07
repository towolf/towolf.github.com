---
layout: mfile
title: RadianceAndPupilAreaEyeLengthToRetIrradiance
categories:
  - PsychRadiometric
encoding: UTF-8
---

retIrradiance\_PowerPerArea = RadianceAndPupilAreaEyeLengthToRetIrradiance(radiance\_PowerPerAreaSr,radianceS,pupilArea,eyeLength)

Perform the geometric calculations necessary to convert a measurement of source
radiance to corresponding retinal irradiance.

Let x be the units of distance (m, cm, mm, um, etc.)

  Input radiance\_PowerPerAreaSr should be in units of power/x^2-sr-wlinterval.
  Input radianceS gives the wavelength sampling information (nm).
  Input pupilArea should be in units of x^2.
  Input eyeLength should be the length of the eye in units of x

  Output retIrradiance\_PowerPerArea is in units of power/x^2-wlinterval.

  Light power may be expressed in watts or quanta-sec or in your
  favorite units.  Indeed, it may also be passed as energy rather
  than power.

This conversion does not take absorption in the eye into account,
as this is more conveniently foldeded into the spectral absorptance.

See also: PsychRadiometric, RetIrradianceAndPupilAreaEyeLengthToRadiance, PupilAreaFromLum, EyeLength.

3/6/13  dhb  Wrote it.