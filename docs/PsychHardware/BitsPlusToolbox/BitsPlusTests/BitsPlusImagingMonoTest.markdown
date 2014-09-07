---
layout: mfile
title: BitsPlusImagingMonoTest
categories:
  - BitsPlusTests
encoding: UTF-8
---

BitsPlusImagingMonoTest([testdrawingcmds])

Test of built-in Mono++ output conversion shader of PTB
imaging pipeline. This is meant to test Bits++ Mono++
conversion of GPU against reference implementation of
Matlab BitsPlus toolbox.

First the stimulus is generated via Matlab conversion routine.
Then it is drawn via PTB imaging pipeline conversion.
Then the PTB imaging result is read back and compared against
the result of the Matlab implementation and the maximum error
is returned. This error should be zero.

The optional parameter 'testdrawingcmds' specs if pure texture
mapping should be tested, or if a combo of texture mapping and
[Screen](/docs/Screen) 2D drawing commands gets tested (1).

THIS TEST IS NOT FINISHED. EARLY BETA.
