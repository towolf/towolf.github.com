---
layout: mfile
title: RetIrradianceToTrolands
categories:
  - PsychRadiometric
encoding: UTF-8
---

[trolands] =...
    RetIrradianceToTrolands(irradianceWatts,irradianceS,[photopic],[species],[source])

Compute trolands from retinal irradiance in watts/um2-wlinterval.  The answer is
returned in trolands/wlinterval and can be summed to get trolands.

See Wyszecki and Stiles, 1982, p. 103 for the conversions.

Input variables: irradianceWatts - retinal irradiance in watts/um2-wlinterval.
                 irradianceS - the wavelength sampling information for the relativeSpectrum.
                 photopic - what kind of trolands: 'Photopic' (Default), 'JuddVos', 'Scotopic'.
                 species, source - passed directly to EyeLength to determine length of eye in mm.
                    These values inherit the default behaviors of EyeLength.

07/18/03  dhb  Wrote it.
04/09/12  dhb  Debug.  This was apparently never quite finished.
               Improve comments.