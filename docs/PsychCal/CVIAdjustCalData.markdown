---
layout: mfile
title: CVIAdjustCalData
categories:
  - PsychCal
encoding: UTF-8
---

calData = CVIAdjustCalData(calData,cviData)

Use the fine spectral measurements taken with
the CVI (see CVIMeasurePhosphors) to adjust
the coarse spectral measurements taken with
the PR-650.  Actually, nothing about the
method is particularly specific to the CVI
and PR-650 devices, but the names in the
structures are coded that way.

1/02/01  dhb, mpr  Wrote it.