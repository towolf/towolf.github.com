---
layout: mfile
title: PR670measxyz
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670measxyz - Make an XYZ measurement with the PR-670.

Syntax:
[xyz, qual] = PR670measxyz

Output:
xyz (3x1) - Measured XYZ values.
qual (scalar) - Measurement quality code.  Will be 0 for successful
    measurements, -8 if too little light.