---
layout: mfile
title: DaqAInScanContinue
categories:
  - Daq
encoding: UTF-8
---

[params, data] = DaqAInScanContinue(DeviceIndex, options [, wantLiveData=0])

Calls DaqAInScan with the options set to only continue, and not begin or
end. You may call DaqAInScanContinue as many times as you like, to keep
transferring reports from the system to PsychHID. Eventually you should
call DaqAInScanEnd to end aquisition and get all remaining data.

If you want to retrieve already captured data, set the optional
'wantLiveData' flag to 1. This will return all already received data in
the optional return argument 'data', in the same format as DaqAInScanEnd
would provide.

See also DaqAInScan, DaqAInScanBegin, DaqAInScanEnd,
Daq, DaqPins, DaqTest, PsychHIDTest.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqAInScanContinue.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqAInScanContinue.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqAInScanContinue.m</code>
</div>
