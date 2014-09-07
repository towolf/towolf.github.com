---
layout: mfile
title: MakeItS
categories:
  - PsychColorimetric
encoding: UTF-8
---

S = MakeItS(wls)

If argument is a [start delta n] description, it is
left alone.

If passed length is not a [start delta n] description,
convert it to one.  Formats handled are a list of evenly
spaced wavelengths or a struct with fields start, step, numberSamples.

Format error checking could be more agressive.

7/26/02  dhb  Allow struct format too.