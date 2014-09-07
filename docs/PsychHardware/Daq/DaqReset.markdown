---
layout: mfile
title: DaqReset
categories:
  - Daq
encoding: UTF-8
---

err=DaqReset(DeviceIndex)
Assuming that something's wrong with the USB-1208FS or our communication
with it, we re-enumerate in order to re-establish communication. Then we
send the reset command to ask the USB-1208FS to reset itself. Then we
re-enumerate again to re-establish communication once more.

To avoid problems caused by CLEAR PsychHID, we recommend that (if you're using
a 1208FS), instead of calling DaqReset, you unplug and reinsert the USB cable
of your USB-1208FS and quit and restart MATLAB. In Denis' experience that
combination always restores normal communication.  If you are using a 1608FS,
keep reading...

This function calls "clear PsychHID" twice, and yet I still frequently found
that I needed to run that command again in order for communication to be
properly established again.  With a USB-1608FS, Matlab 2007b, and Leopard, I
found that I didn't have the problems Denis seemed to have.  But what I did
have was a problem with PsychHID not finding all of the interfaces when
devices were enumerated.  Running this function (followed by an additional
"clear PsychHID" command) worked for me, so my recommendation for that case is
the opposite of Denis'.  I never needed to re-start Matlab or unplug the
device to get my problems solved.  So I recommend you just run this command,
then run "clear PsychHID", then try "daq=DaqFind" or "daqs=DaqDeviceIndex"
(the latter if you have more than one A/D converter built by Measurement
Computing.  -- mpr

On Snow Leopard. Matlab R2010a, I found I could re-establish communication
with an unresponsive 1208FS with the calls above (that is, calling DaqReset
followed by "clear PsychHID") -- sdv

See also Daq, DaqFunctions, DaqPins, DaqTest, PsychHIDTest, DaqFind,
DaqDeviceIndex.