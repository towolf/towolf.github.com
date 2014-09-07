---
layout: mfile
title: PR670getsyncfreq
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670getsyncfreq - Measures the frequency of the light source.

Syntax:
syncFreq = PR655getsyncfreq

Output:
syncFreq (scalar) - The frequency of the light source in Hz.  Is empty if
    PR-670 encounters an error.
errorCode (scalar) - The error code if an error occurs.  Is 0 if no
    error.