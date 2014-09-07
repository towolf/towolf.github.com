---
layout: mfile
title: IsMinimumOSXVersion
categories:
  - PsychOneliners
encoding: UTF-8
---

rc = IsMinimumOSXVersion(major, minor, point);

Checks if the script is running on a MacOS/X system with at least the
requested (major,minor,point) version, e.g., to test for a MacOS/X system
of 10.4.8 or later, do a IsMinimumOSXVersion(10,4,8);

rc is 0 if the system is of a lower version, 1 if it satisfies this
minimum version, 2 if the function doesn't know.