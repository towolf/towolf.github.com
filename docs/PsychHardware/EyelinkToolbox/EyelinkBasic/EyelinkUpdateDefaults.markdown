---
layout: mfile
title: EyelinkUpdateDefaults
categories:
  - EyelinkBasic
encoding: UTF-8
---

USAGE = EyelinkUpdateDefaults(el)

This function passes changes to the calibration defaults structure
to the callback function. To be called after EyelinkInitDefaults if any
changes are made to the output structure of that function.

el=EyelinkInitDefaults(window);
el.backgroundColour = BlackIndex(window);
EyelinkUpdateDefaults(el);

27-1-2011 NJ created
19-12-2012 IA Fix hardcoded callback