---
layout: mfile
title: DaqCIn
categories:
  - Daq
encoding: UTF-8
---

count=DaqCIn(DeviceIndex)  
USB-1208FS: Read counter.  
This function reads the 32-bit event counter in the device. This counter  
tallies the transitions of an external input attached to the CTR pin on  
the screw terminal of the device.  
"count" is the 32-bit value.  
"DeviceIndex" is a small integer, the array index specifying which HID  
      device in the array returned by PsychHID('Devices') is interface 0  
      of the desired USB-1208FS box.  
See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest.  

4/15/05 dgp Wrote it.  
12/20/07  mpr   tested it on a 1608FS and made input argument optional  
1/13/08   mpr   swept through and tried to make terminology consistent  
                    with that of other daq functions  
5/22/08   mk  Add (untested!) support for USB-1024LS box.  
5/23/08   mk  Add caching for HID device list.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/Daq/DaqCIn.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/Daq/DaqCIn.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/Daq/DaqCIn.m</code>
</div>
