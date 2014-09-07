---
layout: mfile
title: DaqTest
categories:
  - PsychTests
encoding: UTF-8
---

DaqTest

DaqTest assesses the Daq Toolbox, which provides communication with a
particular USB data acquisition device (daq): the USB-1208FS made by
Measurement Computing (see URL below). This daq costs $150 and offers "50
kHz" input and output 12-bit sampling of analog voltages (8 in, 2 out)
and 16 digital i/o lines, with signals brought out to screw terminals.
("50 kHz" is a theoretical upper limit: as of 18 April 2005 we attain 2
kHz.) The USB-1208FS is the size of a wallet and is powered through its
USB cable. The Daq Toolbox gives you complete control of it from within
Matlab, via the PsychHID extension.

DaqTest assesses all the functions provided by the USB-1208FS firmware.
(Some risky tests, below, have been turned off, but can be re-enabled by
the adventurous user.) DaqFunctions gives a brief description of every
function.

NOT RESPONDING? If PsychHID is not responding, e.g. after unplugging and
re-plugging the USB connector of your device, try quitting and restarting
MATLAB. We find that this reliably restores normal communication.

<http://www.http://www.measurementcomputing.com/cbicatalog/directory.asp?dept\_id=403>
<http://psychtoolbox.org/daq.html>
See also: Daq, DaqFunctions, DaqPins,PsychHIDTest,PsychHID,PsychHardware,
DaqDeviceIndex, DaqDIn, DaqDOut, DaqAIn, DaqAOut, DaqAInScan, DaqAOutScan


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychTests/DaqTest.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychTests/DaqTest.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychTests/DaqTest.m</code>
</div>
