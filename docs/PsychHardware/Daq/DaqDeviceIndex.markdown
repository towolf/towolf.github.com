---
layout: mfile
title: DaqDeviceIndex
categories:
  - Daq
encoding: UTF-8
---

daq = DaqDeviceIndex([DeviceName][, ShowInterfaceNumberWarning=1])
Returns a list of all your USB -1208FS, -1408FS, or -1608FS daqs.

CAUTION: This routine works well on GNU/Linux and MS-Windows, but is very
unreliable on Apple OSX, especially with multiple DAQ devices connected.
You may be better off guessing a proper daq index.

Also implements experimental code for detection of the USB-1024LS.
However that code has not been tested yet and may need some small amount
of tweaking to make it really work. Search the Psychtoolbox forum for
corresponding messages...

TECHNICAL NOTE: When we call PsychHID('Devices'), each USB-1208FS/1408FS
box presents itself as four HID "devices" sharing the same serial number. They
are interfaces 0,1,2,3. They usually appear in reverse order in the
device list. Nearly all the commands use only interface 0, so
we will select that one to represent the whole. All our Daq routines
expect to receive just the interface 0 device as a passed designator. The
few routines that need to access the other interfaces do so
automatically.

ADDENDUM: The above statement is correct for the 1208FS and the 1408FS,
not for the 1608FS. Number of Devices found by PsychHID for a
1608FS and Leopard varies from five to seven with little rhyme or reason.  It
appears that the correct number of interfaces is seven.  As with the 1208FS,
most communication is through interface 0.  However, when acquiring data
(e.g., using DaqAInScan), output is via interfaces 1 through 6.  Because
PsychHID's enumeration of the interfaces is flaky, you may need to run this
function more than once (with calls to DaqReset and probably "clear PsychHID"
in between successive calls) in order to get device enumeration completed
correctly.  In DaqTest, user will be warned if they try to test a 1608 and
this function doesn't return the right number of interfaces, so I added the
second optional argument as a flag to suppress the warning that would be
generated here. -- mpr

See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest,
DaqFind, DaqDIn, DaqDOut, DaqAIn, DaqAOut, DaqAInScan,DaqAOutScan.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqDeviceIndex.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqDeviceIndex.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqDeviceIndex.m</code>
</div>
