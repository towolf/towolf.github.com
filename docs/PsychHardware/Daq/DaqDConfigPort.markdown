---
layout: mfile
title: DaqDConfigPort
categories:
  - Daq
encoding: UTF-8
---

err=DaqDConfigPort(DeviceIndex,port,direction)
USB-1208FS: Configure digital port. This command sets the direction of
the DIO port to input or output.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
"port" 0 = port A, 1 = port B
"direction" 0 = output, 1 = input

USB-1608FS: has only one port, so second argument is meaningless.  If three
arguments are passed and device is a 1608FS, second argument is ignored.
Function could be made more efficient if a separate one were written for
\1608FS, but I'm guessing this function will never be used at a time when
maximal speed is an overarching requirement.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHidTest.

USB-1024LS: Has three ports, probably numbered: 1 = port A, 4 = port B,
\10 = port C (the sum of: 8 = portC low, 2 = portC high).

\4/15/05   dgp Wrote it.
\12/18/07  mpr extended for 1608
\1/11/08   mpr swept through trying to improve consistency across daq
                functions
\5/22/08   mk  Add (untested!) support for USB-1024LS box.
\5/23/08   mk  Add caching for HID device list.
\8/12/2010 sdv Fixed error when other HID devices have short names


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqDConfigPort.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqDConfigPort.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqDConfigPort.m</code>
</div>
