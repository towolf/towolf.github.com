---
layout: mfile
title: EnergyToQuanta
categories:
  - PsychRadiometric
encoding: UTF-8
---

quanta = EnergyToQuanta(wls,energy)

Convert energy units (energy or power per unit wavelength)
to quantal units (quanta or quanta/sec per unit wavelength).

Constants are set up so that we have energy in joules or
power in watts.  Wavelengths should be passed in nanometers.

The routine is set up to convert spectra.  These are
passed as the columns of the matrix energy.  The
wavelengths corresponding to each row are passed in
the column vector wls.

7/29/96  dhb  Wrote it.
8/16/96  dhb, abp  Modified interface.