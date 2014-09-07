---
layout: mfile
title: DaqReadCode
categories:
  - Daq
encoding: UTF-8
---

data=DaqReadCode(DeviceIndex,address,bytes)
USB-1208FS: Read program memory.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
"address" is a 24-bit address.
"bytes" is the number of bytes to read (up to 62);
See also DaqWriteCode, Daq, DaqTest, PsychHIDTest.