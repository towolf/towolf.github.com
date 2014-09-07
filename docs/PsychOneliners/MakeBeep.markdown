---
layout: mfile
title: MakeBeep
categories:
  - PsychOneliners
---

\[beep,samplingRate\] = MakeBeep\(freq,duration,\[samplingRate\]\)

Compute array that can be used by [Snd](/docs/Snd) to produce a pure tone of specified
"freq" \(Hz\) and "duration" \(s\). The "samplingRate" defaults to
[Snd](/docs/Snd)\('DefaultRate'\).

    beep = MakeBeep\(freq,duration\);
    [Snd](/docs/Snd)\('Open'\);
    .... do some stuff ....
    [Snd](/docs/Snd)\('Play',beep\);

See [Snd](/docs/Snd).


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/MakeBeep.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/MakeBeep.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/MakeBeep.m</code>
</div>
