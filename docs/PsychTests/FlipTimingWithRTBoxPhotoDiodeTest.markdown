---
layout: mfile
title: FlipTimingWithRTBoxPhotoDiodeTest
categories:
  - PsychTests
encoding: UTF-8
---

FlipTimingWithRTBoxPhotoDiodeTest(configFile)

Test visual stimulus onset timing accuracy and visual stimulus onset
timestamping precision and robustness under varying loads, conditions and
modes of operation. This requires one of the supported external
measurement devices to provide the "ground truth" for true stimulus onset
times. Currently supported: UCST RTBox with photo-diode, VPixx Inc. DataPixx,
UBW32/Bitwhacker + UCST VideoSwitcher. Can also be used without external
equipment to just test stimulus onset accuracy with only indirect test of
timestamping.

This documentation is incomplete for now, good luck!

'configFile' Filename of benchmark configuration file.

Mandatory variables in file:
----------------------------

conf.Stereo              = Stereomode to use.
conf.[Priority](/docs/Priority)            = Realtime priority to use.
conf.DWMEnabled          = 1,0,-1 = On, Off, Auto
conf.SetForegroundWindow = 1,0,-1 = On, Off, Auto
conf.VBLTimestampingMode = Mode of high-precision timestamping.
conf.CheckAsyncFlip      = 0,1,2 = Off-Use sync flip, 1 = Use async flip, 2 = Use async flip with polling, 3 = Use async flip with Waituntilasyncflipcertain.

# Per trial parameters for trial i:

conf.waitFramesSched(i)  = Number of ifi's to wait before onset in trial i.
conf.loadjitter(i)       = Max. random cpu load jitter to apply in frame i.
conf.gpuLoad(i)          = Number of rects to draw in frame i (GPU load)