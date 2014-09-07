---
layout: mfile
title: PR705measspd
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705measspd - Get a spectral power distribution from the PR-705.

Syntax:
spd = PR705measspd([S])

Input:
S (1x3) - Desired wavelength sampling. Default: [380 5 81]

Output:
spd (Nx1) - The spectral power distribution (N = S(3) or 81 by default).

12/06/12   zlb   Wrote it loosely based on the PR670Toolbox.