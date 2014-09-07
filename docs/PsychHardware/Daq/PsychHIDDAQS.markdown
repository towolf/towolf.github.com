---
layout: mfile
title: PsychHIDDAQS
categories:
  - Daq
encoding: UTF-8
---

daqdevs = PsychHIDDAQS -- Enumerate and preprocess HID-DAQ device list.

Used as helper by Daq toolbox functions. Retrieves the USB-HID devices
list from PsychHID, prefilters all DAQ device entries, so they have a
well defined productID, product name string and a somewhat unique
serialNumber -- as far as this is possible. Leaves unsupported (non-DAQ)
device entries alone.

It then caches the preprocessed list to save processing time on
successive calls to the function.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/PsychHIDDAQS.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/PsychHIDDAQS.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/PsychHIDDAQS.m</code>
</div>
