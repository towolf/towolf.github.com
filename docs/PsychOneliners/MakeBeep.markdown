---
layout: mfile
title: MakeBeep
categories:
  - PsychOneliners
encoding: UTF-8
---

[beep,samplingRate] = MakeBeep(freq,duration,[samplingRate])

Compute array that can be used by [Snd](/docs/Snd) to produce a pure tone of specified
"freq" (Hz) and "duration" (s). The "samplingRate" defaults to
[Snd](/docs/Snd)('DefaultRate').

    beep = MakeBeep(freq,duration);
    [Snd](/docs/Snd)('Open');
    .... do some stuff ....
    [Snd](/docs/Snd)('Play',beep);

See [Snd](/docs/Snd).