---
layout: mfile
title: BasicSoundFeedbackDemo
categories:
  - PsychDemos
encoding: UTF-8
---

BasicSoundFeedbackDemo([reqlatency=7.5 ms] [,duplex=0])

# THIS IS EARLY ALPHA CODE! IT MAY OR MAY NOT WORK RELIABLY ON YOUR SETUP!
TEST IT WITH MEASUREMENT EQUIPMENT IF YOU DEPEND ON ACCURATE FEEDBACK
TIMING!!!

Demonstrates very basic usage of the new Psychtoolbox sound driver
PsychPortAudio() for audio feedback.

Sound is captured from the default recording device and then - with a
selectable delay - played back via the default output device.

By default, feedback is tried with a latency of 7.5 ms plus hardware and
system inherent delay, but you can ask for a specific latency in msecs by
providing the optional parameter 'reqlatency'. Achievable latency will be
constrained by the capabilities of your hardware. Choosing too low of a
value will create audible artifacts in the sound and the driver may
output warning about 'buffer underflows during streaming refill...'.

Depending on your sound hardware you'll have to either leave 'duplex' at
its default of zero (2 times half-duplex mode) or set it to 1
(full-duplex mode): ASIO driven hardware -- typically on MS-Windows --
will usually need full-duplex mode. On Macintosh OS/X it depends on the
sound hardware. IntelMacs are happy with half-duplex mode, some PowerMacs
may need full-duplex mode.


If you need low-latency, make sure to read "help InitializePsychSound"
carefully or contact the forum.
