---
layout: mfile
title: DaqMemRead
categories:
  - Daq
encoding: UTF-8
---

\[data,\[errorstructure\]\]=DaqMemRead\(DeviceIndex,address,bytes\)
USB-1208FS: Read memory. This command reads data from the configuration
memory \(EEPROM\).  All of the memory may be read.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID\('Devices'\) is interface 0
      of the desired USB-1208FS box.
"address" is the 16-bit start address for the read.
"bytes" is the number of bytes to be read, up to a maximum of 62.

Several functions called by this function may produce errors, so
errorstructure is a vector.  It is only returned if the function is called
with two output arguments.
See also DaqWriteCode, DaqMemWrite, Daq, DaqTest, PsychHidTest.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqMemRead.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqMemRead.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqMemRead.m</code>
</div>
