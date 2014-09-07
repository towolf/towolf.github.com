---
layout: mfile
title: BasicToneMapCalFormat
categories:
  - PsychCal
encoding: UTF-8
---

outputXYZCalFormat = BasicToneMapCalFormat(inputXYZCalFormat, maxLum)

Simple tone mapping.  Leaves any pixel with luminance below maxLum alone.
For pixels whose luminance exceeds maxLum, scale XYZ down multiplicatively so
that luminance is maxLum.

10/1/09 bjh, dhb     Created it.
10/4/09 dhb          Debug and make it work right.