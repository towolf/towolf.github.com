---
layout: mfile
title: PR705parsespdstr
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705parsespdstr - Parses the spectral power distribution string returned by the PR-705.

Syntax:
spd = PR705parsespdstr(rawspd [, S])

Description:
Parse the spectral power distribution string returned by the PR-705. The
results are splined to the desired wavelength sampling defined by the 'S'
input parameter.

Input:
rawspd (1xN char) - Raw data returned from a meter measurment.
S (1x3) - Wavelength sampling.  Default: [380 5 81]

12/06/12    zlb   Wrote it based on the PR670Toolbox.