---
layout: mfile
title: SettingsToSensorAcc
categories:
  - PsychCal
encoding: UTF-8
---

[sensor,primaryE] = SettingsToSensorAcc(cal,settings)

Convert from device setting coordinates to
sensor color space coordinates.  Uses full
basis function measurements in doing
conversions so that it can compensate for
device primary spectral shifts.