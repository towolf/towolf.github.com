---
layout: mfile
title: PrintPhotoreceptors
categories:
  - PsychColorimetricData
encoding: UTF-8
---

PrintPhotoreceptors(photoreceptors)

Print to command window an interpretable output
of what is in a photoreceptors structure.

See also DefaultPhotoreceptors, FillInPhotoreceptors.

7/19/13  dhb  Wrote it.
8/12/13  dhb  Code more generally and get rid of some special cases.
         dhb  For cmf-like spectral functions, print out peak wavelengths and peak values.
10/16/13  mk  fields() -\> fieldnames() for Octave compatibility. Other
              bug fixes, e.g., wrong use of ii for innermost for-loops.