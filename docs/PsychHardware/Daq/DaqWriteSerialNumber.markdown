---
layout: mfile
title: DaqWriteSerialNumber
categories:
  - Daq
encoding: UTF-8
---

err=DaqWriteSerialNumber(DeviceIndex,serialstring)
USB-1208FS: Write a new serial number (an 8-character string) to the
device. The serial number consists of 8 bytes, typically ASCII numeric or
hexadecimal digits (i.e. '00000001'.)  The new serial number will be
programmed but not used until hardware reset. As far as I know, the only
use of the serial number is to distinguish multiple USB-1208FS devices
attached to the same computer.
See also DaqWriteCode, Daq, DaqTest, PsychHIDTest.