---
layout: mfile
title: SleepSecs
categories:
  - PsychObsolete
encoding: UTF-8
---

SleepSecs(s)

Wait for duration s seconds, up to one second.  SleepSecs suspends the
MATLAB process.

# OS X

If you set the priority level to greater than 0 using either [Priority](/docs/Priority) or
[Rush](/docs/Rush) then use SleepSecs instead of WaitSecs while priority is elevated.
Whereas SleepSecs surrenders CPU time,  WaitSecs consumes CPU time,
exceeding limits set by [Priority](/docs/Priority) or [Rush](/docs/Rush) and causing the Mach kernel to
revoke any priority setting greater than 0.

If you are playing an animation, then use [Screen](/docs/Screen)('[Flip](/docs/Flip)') to both
synchronize updating of the display to the Video BLanking invterval (VBL)
and to delay your animation loop until the next VBL; Like SleepSecs, [Flip](/docs/Flip)
surrenders CPU time to other processes, abiding by limits set when
negotiating with the kernel for priority levels > 0.

You should not need to continuously sleep the MATLAB process at high
priority for periods greater than 1 second.  If you feel the need for
continuous  delay at elevated priority for greater than the maximum one
second duration of SleepSecs, consider instead lowering priority to 0,
calling WaitSecs, and then reeleveting priority.

SleepSecs would be useful in a loop which called KbCheck at high priority
while not displaying an animation.

SleepSecs uses the Posix usleep ("microsleep") function.

# OS 9

SleepSecs does not exist in OS 9.

# WINDOWS

SleepSecs does not exist in Windows.
----

See Also: [Priority](/docs/Priority), [Rush](/docs/Rush), SetMachPriorityMex, GetMachPriorityMex, [Screen](/docs/Screen)('[Flip](/docs/Flip)')



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychObsolete/SleepSecs.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychObsolete/SleepSecs.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychObsolete/SleepSecs.m</code>
</div>
