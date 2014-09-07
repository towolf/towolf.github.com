---
layout: mfile
title: PR705rawspd
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705rawspd - Takes an spd measurement and returns the results.

Syntax:
rawspd = PR705rawspd(timeout)

Input:
timeout (scalar) - Timeout period in seconds.

Output:
rawspd (1xN char) - The raw character array resulting from a measurement.
This will be an empty string if the timeout period was reached.
errcode (scalar) - The error code reported by the meter (success = 0).

12/06/12   zlb   Wrote it.