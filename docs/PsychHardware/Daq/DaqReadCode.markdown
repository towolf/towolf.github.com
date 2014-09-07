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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqReadCode.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqReadCode.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqReadCode.m</code>
</div>
