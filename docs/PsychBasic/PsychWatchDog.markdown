---
layout: mfile
title: PsychWatchDog
categories:
  - PsychBasic
---

PsychWatchDog \- Watchdog mechanism and error handler for Psychtoolbox.

PsychWatchDog\(\[heartbeat\]\);

PsychWatchDog implements a watchdog timer under GNU/Octave. It is not
supported under the Matlab runtime environment yet.

After PsychWatchDog is enabled, it will become active as soon an Octave
waits for user input, either via some keyboard input command within a
script, or when the command prompt becomes active after a script has
finished running, or been terminated by an error or a users CTRL\+C
interrupt.

It will respond to the user pressing CTRL \+ . by closing all open
onscreen windows. If a timeout was set, it will also automatically close
all windows if the timeout is reached without a sign of life from the
users script.

# Usage:

1. Call PsychWatchDog\(heartbeat\) once at the beginning of your script to
enable the watchdog. A 'heartbeat' value of zero will only enable
watching for CTRL \+ . key press. A 'heartbeat' value \> 0 will set the
timeout to 'heartbeat' seconds.

2. Periodically call PsychWatchDog; without arguments in your script to
tell the watchdog that your code is still running properly. If Octave
waits for input and more than 'heartbeat' seconds elapse since the last
PsychWatchDog call, then the watchdog will trigger and close all windows.

3. At the end of your script, call PsychWatchDog\(\-1\); to disable the
watchdog again.

You can call PsychWatchDog\(\) with a vector of at least 2 keycodes as
delivered by KbName to change the abort key combo from CTRL \+ . to some
other arbitrary two key combination. E.g., ...
PsychWatchDog\(\[KbName\('ESCAPE'\), KbName\('q'\)\]\);
... would change the abort key combo to ESCape key \+ q key.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/PsychWatchDog.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/PsychWatchDog.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/PsychWatchDog.m</code>
</div>
