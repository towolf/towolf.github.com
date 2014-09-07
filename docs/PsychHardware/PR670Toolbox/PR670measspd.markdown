---
layout: mfile
title: PR670measspd
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670measspd - Make a measurement measurement.

Syntax:
[spd, qual] = PR670measspd(S)
[spd, qual] = PR670measspd(S, syncMode)

Input:
S (1x3) - Desired wavelength sampling. Default: [380 5 81]
syncMode (string) - Toggles syncronization with the light source.  Set
    using the strings 'on' or 'off'.  Default: 'on'

Output:
spd (Mx1) - Light source spectrum.
qual (scalar) - Measurement quality code.  See the PR-670 manual.