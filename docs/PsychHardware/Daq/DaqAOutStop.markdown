---
layout: mfile
title: DaqAOutStop
categories:
  - Daq
encoding: UTF-8
---

err=DaqAOutStop(DeviceIndex)
USB-1208FS stop analog output scan.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
See also Daq, DaqFunctions, DaqPins, DaqAOutScan, DaqTest,
PsychHIDTest.