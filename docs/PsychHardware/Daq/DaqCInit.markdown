---
layout: mfile
title: DaqCInit
categories:
  - Daq
encoding: UTF-8
---

err=DaqCInit(DeviceIndex)
USB-1208FS: Initialize counter to zero.
"DeviceIndex" is a small integer, the array index specifying which HID
        device in the array returned by PsychHID('Devices') is interface 0
        of the desired USB-1208FS box.
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest.

4/15/05 dgp Wrote it.
12/20/07  mpr   tested it on 1608FS and then made input argument optional
1/10/08   mpr   swept through trying to improve consistency across Daq
                    functions
5/22/08   mk  Add (untested!) support for USB-1024LS box.
5/23/08   mk  Add caching for HID device list.