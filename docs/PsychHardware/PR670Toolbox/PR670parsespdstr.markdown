---
layout: mfile
title: PR670parsespdstr
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670parsespdstr - Parses the  spectral power distribution string returned by the PR-670.

Syntax:
spd = PR670parsespdstr(readStr)
spd = PR670parsespdstr(readStr, S);

Description:
Parse the spectral power distribution string returned by the PR-670.  The
results are splined to the desired wavelength sampling defined by the 'S'
input parameter.

Input:
readStr (1xN char) - Raw data returned from a meter measurment.
S (1x3) - Wavelength sampling.  Default: [380 5 81]