---
layout: mfile
title: uvTols
categories:
  - PsychColorimetric
encoding: UTF-8
---

ls = [uvTols](/docs/uvTols)(uv)

Convert CIE u'v' chromaticity to cone chromaticity ls, L/(L+M+S), S/(L+M+S).

Uses regression conversion matrix based on Judd-Vos XYZ and
Smith-Pokorny cone fundamentals to get from XYX to LMS.  This
is an exact linear transformation and so you don't get as many
weird little numerical things happening when you apply this to
uv for spectral lights.

3/17/04  dhb        Wrote it.
05/06/11 dhb      Make function name in file match actual function name.