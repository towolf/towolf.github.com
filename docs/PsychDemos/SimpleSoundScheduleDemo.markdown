---
layout: mfile
title: SimpleSoundScheduleDemo
categories:
  - PsychDemos
encoding: UTF-8
---

SimpleSoundScheduleDemo - Show simple application of sound schedules.

This demo shows a very basic application of PsychPortAudio's sound
schedule functions. It defines a sequence of 1 second beep tones which are
supposed to be emitted at specific times relative to some trigger event,
e.g., 5 seconds, 10 seconds and 15 seconds after the trigger event. The
trigger event here is a key press, but could be something else like a
visual stimulus onset or reception of some other external trigger signal.

The demo performs 3 trials, each waiting for a keypress, then executing
the 3 beep tone schedule. After those 3 trials it exits.

For more complex applications and use of sound schedules see
BasicSoundScheduleDemo. For a complex mixture with audio mixing, see
BasicAMAndMixScheduleDemo.
