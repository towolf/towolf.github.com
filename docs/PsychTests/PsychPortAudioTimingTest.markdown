---
layout: mfile
title: PsychPortAudioTimingTest
categories:
  - PsychTests
encoding: UTF-8
---

PsychPortAudioTimingTest([exactstart=1][, deviceid=-1][, latbias=0][, waitframes=1][, useDPixx=0][, triggerLevel=0.01])

Test script for sound onset timing reliability and sound onset
latency of the PsychPortAudio sound driver.

This script configures the driver for low latency and high timing
precision, then executes ten trials where it tries to emit a beep sound,
starting in exact sync to a black-white transition on the display.

You'll need measurement equipment to use this: A photo-diode attached to
the top-left corner of your CRT display, a microphone attached to your
speakers, some oszillograph to record and measure the signals from the
diode and microphone.

Some parameters may need tweaking. Make sure you got a setup as described
in 'help InitializePsychSound' for best results.

# Optional parameters:

'exactstart' = 0 -- Start immediately, measure absolute latency.
             \= 1 -- Test accuracy of scheduled sound onset. (Default)

'deviceid'   = -1 -- Auto-select optimal device (Default).
            \>=0   -- Select specified output device. See
                     PsychPortAudio('GetDevices') for a list of devices.

'latbias'    = Hardware inherent latency bias. To be determined by
               measurement - allows to PA to correct for it if provided.
               Unit is seconds. Defaults to zero.

'waitframes' = Time to wait (in video refresh intervals) before emitting beep + flash.
               Defaults to a value of 1, may need to be set higher for
               high latency sound hardware (where absolute latency \> 1
               video refresh duration).

'useDPixx'   = 1 -- Use DataPixx device to automatically measure the true
                    audio onset time wrt. to visual stimulus onset.
               0 -- Don't use DataPixx. This is the default.

'triggerLevel' = Sound signal amplitude for DataPixx to detect sound
                 onset. Defaults to 0.01 = 1% of max amplitude if
                 exactstart == 0, otherwise it is auto-detected by
                 calibration. This will likely need tweaking on your
                 setup. If the measured audio onset delta by DataPixx is
                 much lower (or almost zero) than the expected delta
                 reported by PsychPortAudio, then the triggerLevel may be
                 too low and you should try if slightly higher thresholds
                 help to discriminate signal from noise. Too high values
                 may cause a hang of the script. In practice, levels
                 between 0.01 and 0.1 should yield good results. Setting
                 the 'useDPixx' flag to 2 also plots the waveforms
                 captured by DataPixx, which may help in selection of the
                 optimal triggerLevel.
