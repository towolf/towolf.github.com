---
layout: mfile
title: DaqGetStatus
categories:
  - Daq
encoding: UTF-8
---

status=DaqGetStatus(DeviceIndex)
USB-1208FS: Retrieve device status.
"status.master" =0 sync slave; 1 sync master.
"status.rising" =0 trigger on falling edge; 1 trigger on rising edge.
"status.program" =1 program memory update mode.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqGetStatus.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqGetStatus.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqGetStatus.m</code>
</div>
