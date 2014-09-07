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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqWriteSerialNumber.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqWriteSerialNumber.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqWriteSerialNumber.m</code>
</div>
