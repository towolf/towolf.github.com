---
layout: mfile
title: BasicSoundOutputDemo
categories:
  - PsychDemos
encoding: UTF-8
---

BasicSoundOutputDemo\(\[repetitions=0\]\[, wavfilename\]\)

Demonstrates very basic usage of the new Psychtoolbox sound output driver
PsychPortAudio\(\). PsychPortAudio is a completely new sound output driver
for Psychtoolbox, meant as a better, more reliable, more accurate
replacement for the old Psychtoolbox SND\(\) function and other means of
sound output in Matlab like sound\(\), soundsc\(\), wavplay\(\), audioplayer\(\)
etc.

PsychPortAudio is currently only available for OS/X on Intel based
Macintosh computers and for Microsoft Windows. OS/X PowerPC and Linux
will follow in the foreseeable future. The driver is in early beta stage,
fine-tuning, testing and validation will take some time. If you need
sound output, give it a try but don't be disappointed if it doesn't work
perfect, instead report issues to the forum. We don't expect any trouble
on OS/X, but given the huge variability on the Windows platform \(and the
low quality of many sound drivers on Windows\), that may need some tweaking,
so please provide feedback\!

This demo only demonstrates normal operation, not the low-latency mode,
extra demos and tests for low-latency and high precision timing output will
follow soon. If you need low-latency, make sure to read "help
InitializePsychSound" carefully or contact the forum.
Our preliminary testing for low-latency mode showed that sub-millisecond
accurate sound onset and << 10 msecs latency are possible on OS/X and on
some specially configured M$-Windows setups.


# Optional arguments:

repetitions = Number of repetitions of the sound. Zero = Repeat forever
\(until stopped by keypress\), 1 = Play once, 2 = Play twice, ....

wavfilename = Name of a .wav sound file to load and playback. Otherwise
the good ol' handel.mat file \(part of Matlab\) is used.

The demo just loads and plays the soundfile, waits for a keypress to stop
it, then quits.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/BasicSoundOutputDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/BasicSoundOutputDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/BasicSoundOutputDemo.m</code>
</div>
