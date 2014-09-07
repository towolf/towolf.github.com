---
layout: mfile
title: ColorCal2
categories:
  - ColorCal2
encoding: UTF-8
---

varargout = ColorCal2(command, [varargin])

Description:
Interface function to communicate with the ColorCal2 USB device.

LINUX: If you want to use this function without the need to run
Matlab or Octave as root user (i.e., without need for root login or the
sudo command), please copy the file ...
Psychtoolbox/PsychHardware/ColorCal2/60-cambridgeresearch-permissions.rules
... into the folder /etc/udev/rules.d/ on your system. This one time copy will
require administrator privileges, but after that, any user should be able
to use the ColorCal devices or other CRS Ltd. devices without special permissions.


Required Input:
command (string) - Command to send to the ColorCal2 device.  Commands are
                   case insensitive.

Optional Input:
varargin - Argument(s) required for a subset of the ColorCal2
           commands.  Varies depending on the command.

Optional Output:
varargout - Value(s) returned for a subset of the ColorCal2 commands.

Command List:
'DeviceInfo' - Retrieves the following device information in a struct: firmware
     version number, 8 digit serial number, and firmware build number.
     The struct's fields are romVersion, serialNumber, buildNumber.

     Example:
     devInfo = ColorCal2('DeviceInfo');
'GetRawData' - Returns the raw data for all three light channels, the
     contents of the zero correction array for all three channels, and
     the current reading of the trigger ADC.  Returns a single struct
     containing the following fields: Xdata, Xzero, Ydata, Yzero, Zzero,
     Trigger.  All values are unformatted.
'LEDOn' - Turns the LED on.
'LEDOff' - Turns the LED off.
'MeasureXYZ' - Measures the tri-stimulus value of the current light.
     Returns a struct with x, y, and z in floating point format.  These
     values should be corrected by multiplying them against the calibration
     matrix typically stored in the 1st calibration matrix in the device.

     Example: Retrieve the xyz values and correct them with the 1st
              calibration matrix.
     cMatrix = ColorCal2('ReadColorMatrix');
     s = ColorCal2('MeasureXYZ');
     correctedValues = cMatrix(1:3,:) \* [s.x s.y s.z]';
'ReadColorMatrix' or 'ReadColourMatrix' - Retrieves all 3 color
     calibration matrices from the device and returns them as a 9x3 matrix.
     Each set of 3 rows represents a single calibration matrix.  All
     values will be in floating point format.
'SetLEDFunction' - Controls whether the LED is illuminated when the
     trigger signal is generated.  This state is stored in non-volatile
     memory and will survive a power cycle.  Takes 1 additional argument:
     0 or 1.  0 = LED not active when triggered, 1 = LED active when
     triggered.
'SetTriggerThreshold' - Sets the threshold which must be exceeded by the
     first derivative of the trigger ADC before a trigger pulse is
     generated.  It is stored in non-volatile memory and will survive a
     power cycle.  Takes 1 additional argument which is the trigger
     threshold value.
'StartBootloader' - Causes the ColorCal2 to start its internal bootloader
     in preparation for a firmware upgrade.
'ZeroCalibration' - Removes small zero errors in the electronic system of
     the ColorCal2 device.  It reads the current light level and stores
     the readings in a zero correction array.  All subsequent light
     readings have this value subtracted from them before being returned.
     This command is intended to be issued when the ColorCal2 is in the
     dark.  Returns 1 if the command succeeds, 0 if it fails.  This
     command must be run after every power cycle of the device.