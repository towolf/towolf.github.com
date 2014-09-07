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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqAInStop.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqAInStop.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqAInStop.m</code>
</div>
