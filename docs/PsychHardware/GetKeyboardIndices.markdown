---
layout: mfile
title: GetKeyboardIndices
categories:
  - PsychHardware
encoding: UTF-8
---

[keyboardIndices, productNames, allInfos] = GetKeyboardIndices([productName][, serialNumber][, locationID])

The PsychHID assigns each USB HID device connected to you computer a
unique index. GetKeyboardIndices returns the indices for those HID
devices which are keyboards.  The product names of each keyboard are
returned in a second argument which is useful to identify the keyboard
associated with an index. The third return argument is a cell-array with
complete information about the keyboard device, e.g., allInfos{1} returns
all known info about the 1st detected keyboard.

If you have multiple keyboards connected you can restrict the set of
returned keyboard by specifying the following optional match-critera:

product      = Product name of target devices, as returned in 'productNames'.

serialNumber = Serial number of target devices. This is a text string,
               not a number!

locationID   = Numeric id of where the device is connected to the
               computer. The number is supposed to be unique for a given
               connection port. E.g., the same number will be returned
               whenever the device is connected to the same USB port of
               the computer. The value should be persistent across
               reboots of the machine, but may not be persistent across
               operating system upgrades - or may not be persistent at
               all in case of os bugs. Your mileage may vary...

# WINDOWS, LINUX

GetKeyboardIndices does not yet exist in Windows and Linux.
----

see also: GetGamepadIndices