---
layout: mfile
title: PsychSetupCamera
categories:
  - PsychVideoCapture
encoding: UTF-8
---

PsychSetupCamera(camsettingsfile, rate)

Setup basic camera settings like exposure time, brightness and gain.

The routine loads camera settings from 'camsettingsfile' if it
exists, otherwise it uses the cameras default settings.

Then it runs a video loop at 'rate' frames per second.

# During the loop, the user can change settings by pressing:

'Cursor left' and 'Cursor right' keys to decrease or increase
exposure time.

'Cursor up' and 'Cursor down' to increase or decrease camera gain.

'b' and 'd' to increase or decrease brightness setting.

'w' to write the current settings to 'camsettingsfile', overwriting
the old file, if it already exists.

'ESC'ape key to finish setup.

If no rate is given, the loop runs at 30 Hz.
If no filename is given, 'CamSettings.mat' is read/written from
the current working directory.