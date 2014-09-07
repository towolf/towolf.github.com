---
layout: mfile
title: DaqPrepareDownload
categories:
  - Daq
encoding: UTF-8
---

err=DaqPrepareDownload\(DeviceIndex,\[ProgramModeFlag\]\)
USB-1208FS: Prepare for program memory download. This command puts the
device into code update mode.  The unlock code must be correct as a
further safety device.  Call this once before sending code with
WriteCode.  If not in code update mode, any WriteCode commands will be
ignored. The USB-1208FS firmware manual does not state how long the "code
update mode" state persists, or how it can be turned back off. However, the
DaqGetStatus command does report this state.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID\('Devices'\) is interface 0
      of the desired USB-1208FS box.
See also DaqWriteCode, Daq, DaqTest, PsychHIDTest.

In my tests with a USB-1608FS, sending a report with anything other than the
correct unlock code caused the device to exit program mode.  So I modified
this function to allow user to toggle between states. If no second argument is
passed, function assumes user wants to put device into program mode; else if
second argument is zero device will be taken \(or left\) out of program mode.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqPrepareDownload.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqPrepareDownload.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqPrepareDownload.m</code>
</div>
