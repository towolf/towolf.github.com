---
layout: mfile
title: EyelinkInitDefaults
categories:
  - EyelinkBasic
encoding: UTF-8
---

Initialize eyelink defaults and control code structure

USAGE: el=EyelinkInitDefaults([window])

      window is optional windowPtr.
      If set, pixel coordinates are send to eyetracker

and fill it with some sensible values.
Note that these values are only used by the m-file
versions of dotrackersetup and dodriftcorrect.