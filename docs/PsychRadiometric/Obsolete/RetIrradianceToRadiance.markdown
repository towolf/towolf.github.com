---
layout: mfile
title: RetIrradianceToRadiance
categories:
  - Obsolete
encoding: UTF-8
---

radianceWattsPerM2Sr = RetIrradianceToRadiance(irradianceWattsPerUm2,irradianceS,pupilAreaMm2,eyeLengthMm)

Perform the geometric calculations necessary to convert a measurement of retinal
irradiance to the source radiance that would produce it.

  Input irradianceWattsPerUm2 is in units of power/um^2-wlinterval.
  Input irradianceS gives the wavelength sampling information.
  Input pupilAreaMm2 should be in units of mm^2.
  Input eyeLengthMm should be the length of the eye in mm.
  Output radianceWattsPerM2Sr is in units of power/m^2-sr-wlinterval.

  Light power may be expressed in watts or quanta-sec or in your
  favorite units.  Indeed, it may also be passed as energy rather
  than power.

This conversion does not take absorption in the eye into account,
as this is more conveniently foldeded into the spectral absorptance.

See also: RetIrradianceAndPupilAreaEyeLengthToRadiance

Note: This routine is now obsolete, as it mixes radiometric and unit conversions.  Preferred is to
use RadianceAndPupilAreaEyeLengthToRetIrradiance and then take charge of your units in your
calling code.

2/28/13  dhb  Wrote it.
3/6/13   dhb  Rewrite to use new conversion function.  Move to Obsolete directory.
         dhb  Also improved variable naming.