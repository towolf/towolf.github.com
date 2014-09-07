---
layout: mfile
title: get_color
categories:
  - Utilities
encoding: UTF-8
---

Syntax: ColorVector = get\_color(ColorNameString)

convert color name to color triple. Color name/triple combinations
were taken from the Unix X11/R4 rgb.txt file and converted to
a format matlab would properly interpret.  This function was
created by Mickey P. Rowe some time around 1993 or 1994.  In June of 2000
I found out that the switch statement could be used instead of successive
calls to strcmp.  I suspect that the compiled version is identical, but this
looks more elegant.