---
layout: mfile
title: DaqBlinkLED
categories:
  - Daq
encoding: UTF-8
---

err=DaqBlinkLED(DeviceIndex)
USB-1208FS: blink LED.
"DeviceIndex" is a small integer, the array index specifying which HID
      device in the array returned by PsychHID('Devices') is interface 0
      of the desired USB-1208FS box.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest.

4/15/05 dgp Wrote it.
11/13/07  mpr Tested it on USB-1608FS called by Matlab 2007b from a Mac
                  Pro running Leopard.  Worked with no changes!
1/10/08   mpr worked to get improved internal consistency (changed
                  "device" to "daq", fixed "TestDaq" and "TestPsychHid"
5/22/08   mk  Add (untested!) support for USB-1024LS box.
5/23/08   mk  Add caching for HID device list.