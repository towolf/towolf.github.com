---
layout: mfile
title: DaqAOut
categories:
  - Daq
encoding: UTF-8
---

err=DaqAOut(DeviceIndex,channel,v)
USB-1208FS analog output.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
"channel" is 0 or 1.
"v" is a value in the range 0 to 1, which will produce an output voltage
      in the range 0 to 4.095 V.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest,
DaqDeviceIndex, DaqDIn, DaqDOut, DaqAIn, DaqAInScan, DaqAOutScan.