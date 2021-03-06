---
layout: mfile
title: DaqGetAll
categories:
  - Daq
encoding: UTF-8
---

data=DaqGetAll(DeviceIndex)
USB-1208FS: Retrieve all analog and digital input values. This command
reads the value from all analog input channels and digital I/Os.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
data.analog is a 1x16 array of the values read from the analog input
      channels.
data.digital(1) is the value (0 to 255) read from digital port A.
data.digital(2) is the value (0 to 255) read from digital port B.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest.