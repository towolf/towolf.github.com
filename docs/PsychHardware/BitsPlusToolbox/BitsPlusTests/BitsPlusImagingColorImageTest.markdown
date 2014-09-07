---
layout: mfile
title: BitsPlusImagingColorImageTest
categories:
  - BitsPlusTests
encoding: UTF-8
---

BitsPlusImagingColorImageTest([realimage][, imagefile][, plotdiffs])

Test use of Color++ mode with imaging pipeline...

Renders a HDR color image, converts it to Bits++ Color++ format, once via
Matlab Bits++ toolbox function BitsPlusPackColorImage and once via GPU
based imaging pipeline. Reads back and compares results to assess
correctness and accuracy of the new GPU implementation.

realimage = 0 (Default) Create color gradient pattern with all 65535
possible values for a systematic test.

realimage = 1 Load an example HDR image of a "real" rendered scene for
comparison.

# UNFINISHED BETA CODE!
