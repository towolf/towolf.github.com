---
layout: mfile
title: PsychHIDTest
categories:
  - PsychTests
encoding: UTF-8
---

PsychHIDTest

PsychHIDTest exercises the PsychHID mex file. We list all the HID
devices. We read from the keyboard and mouse. We flicker the keyboard
LEDs.

On MS-Windows we only list the HID devices, as mouse and keyboard are
not really accessible for PsychHID on MS-Windows.

NOT RESPONDING? If PsychHID is not responding, e.g. after unplugging and
re-plugging the USB connector, try quitting and restarting MATLAB. We
find that this reliably restores normal communication.

<http://psychtoolbox.org/usb.html>
See also DaqTest, PsychHID, PsychHardware.