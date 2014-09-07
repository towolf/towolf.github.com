---
layout: mfile
title: DaqSetCal
categories:
  - Daq
encoding: UTF-8
---

err=DaqSetCal\(DeviceIndex,on\)
USB-1208FS set CAL output.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID\('Devices'\) is interface 0
      of the desired USB-1208FS box.
"on" is 1 for on \(+2.5 V\), and 0 for off \(0 V\).
USB-1608FS:
arguments and logic are the same except that "on" can take more values to
produce a wider variety of results:

on                    output \(Volts\)
---                   ------
 0                       0
 1                     0.625
 2                      1.25
 3                      2.5
 4                        5

The calibration terminal is pin 17 on the USB-1608FS.

See also Daq, DaqFunctions, DaqPins, ,DaqCalibrateAIn, DaqTest, PsychHIDTest.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqSetCal.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqSetCal.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqSetCal.m</code>
</div>
