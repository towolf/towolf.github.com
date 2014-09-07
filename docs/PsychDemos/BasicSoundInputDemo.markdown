---
layout: mfile
title: BasicSoundInputDemo
categories:
  - PsychDemos
---

BasicSoundInputDemo\(\[wavfilename\] \[, voicetrigger=0\] \[, maxsecs=inf\]\)

Demonstrates very basic usage of the new Psychtoolbox sound driver
PsychPortAudio\(\) for audio capture / recording.

Sound is captured from the default recording device, optionally waiting
until the amplitude exceeds some threshold level before start of
recording. At the end of the recording session the recorded sound is
played back vie the default output device. Waveform data of captured
sound is also plotted to a Matlab figure window during capture.

This demo only demonstrates normal operation, not the low\-latency mode,
extra demos and tests for low\-latency and high precision timing output will
follow soon. If you need low\-latency, make sure to read "help
InitializePsychSound" carefully or contact the forum.
Our preliminary testing for low\-latency mode showed that sub\-millisecond
accurate sound onset and << 10 msecs latency are possible on OS/X and on
some specially configured M$\-Windows setups.


# Optional arguments:

wavfilename = Name of a .wav sound file to store the recorded sound to.
              If left out, sound won't be stored to filesystem.

voicetrigger = If set to a non\-zero threshold value, the driver will wait
               for the sound signal to exceed the specified voicetrigger threshold
               level before it starts capturing audio data.

maxsecs      = Maximum number of seconds of sound to capture. Defaults to
               infinite \- sound is recorded until a key is pressed.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/BasicSoundInputDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/BasicSoundInputDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/BasicSoundInputDemo.m</code>
</div>
