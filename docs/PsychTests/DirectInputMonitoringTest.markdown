---
layout: mfile
title: DirectInputMonitoringTest
categories:
  - PsychTests
encoding: UTF-8
---

DirectInputMonitoringTest - Test "Zero latency direct input monitoring" feature of some sound cards.

This test will currently only work on a subset of some ASIO 2.0 capable
soundcards on Microsoft Windows operating systems with the latest
PsychPortAudio driver and portaudio\_x86 ASIO enabled plugin from the
Psychtoolbox Wiki.

The test allows you to exercise Direct input monitoring features on your
soundcard if the card supports them.

Use ESCape to exit. Space to toggle mute/unmute. 'i' key to change input
channel to monitor, 'o' key to select output channel for monitoring. Use
Cursor Up/Down to increase and decrease amplifier gain. Use Left/Right
cursor keys to change stereo panning. The 'p' key puts the device into a
fake playback mode.
