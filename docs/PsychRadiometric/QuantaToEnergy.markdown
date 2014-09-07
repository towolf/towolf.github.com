---
layout: mfile
title: QuantaToEnergy
categories:
  - PsychRadiometric
encoding: UTF-8
---

energy = QuantaToEnergy(wls,quanta)

Convert quantal units (quanta per unit wavelength)
to energy units (energy or power per unit wavelength).

Constants are set up so that we have energy in joules or
power in watts.

The routine is set up to convert spectra.  These are
passed as the columns of the matrix quanta.  The
wavelengths corresponding to each row are passed in
the column vector wls.

\7/29/96  dhb  Added comment.
\8/16/96  dhb, abp  Modified interface.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/QuantaToEnergy.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/QuantaToEnergy.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/QuantaToEnergy.m</code>
</div>
