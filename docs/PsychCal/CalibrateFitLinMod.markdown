---
layout: mfile
title: CalibrateFitLinMod
categories:
  - PsychCal
encoding: UTF-8
---

cal = CalibrateFitLinMod(cal)

Fit the linear model to spectral calibration data.

3/26/02  dhb  Pulled out of CalibrateMonDrvr.
3/27/02  dhb  Add case of nPrimaryBases == 0.
2/15/10  dhb  Fix so that first basis vector is good approximation to max
              input primary spectrum.
         dhb  Normalize basis vectors so that their max power matches that
              of first component.
4/30/10  dhb  Execute yoked fit if yokedGamma flag is set.
5/25/10  dhb, ar Change yoked field names to match
5/26/10  dhb, ar Still fussing with names.
5/28/10  dhb, ar Pull out yoked fitting from here -- too confusing.
5/27/12  dhb     Handle case where there are more measurements than wavelength samples.