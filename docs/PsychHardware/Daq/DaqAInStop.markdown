---
layout: mfile
title: DaqAInStop
categories:
  - Daq
encoding: UTF-8
---

err=DaqAInStop(DeviceIndex)
USB-1208FS stop analog input scan. You probably will never need to
explicitly call this function because it's already called on your behalf
by DaqAInScan and DaqAInScanEnd.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
See also Daq, DaqFunctions, DaqPins, DaqAInScan.