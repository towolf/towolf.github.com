---
layout: mfile
title: DaqMemWrite
categories:
  - Daq
encoding: UTF-8
---

err=DaqMemWrite(DeviceIndex,address,data)
USB-1208FS: Write memory. This command writes to the nonvolatile EEPROM
memory on the device. The nonvolatile memory is used to store
calibration coefficients, system information, and user data.  Locations
0x000 to 0x07F are reserved for firmware use and may not be written.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
"address" is the 16-bit start address for the write.
"data" is a vector with length up to 59, one element per byte.
See also DaqWriteCode, DaqMemRead, Daq, DaqTest, PsychHIDTest.