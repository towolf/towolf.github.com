---
layout: mfile
title: KbQueueReserve
categories:
  - PsychBasic
encoding: UTF-8
---

Reserve the keyboard queue of the default keyboard for use by the
alternative GetChar() implementation. This is for internal use only!

'action': 1 = Try to reserve, 2 = Try to release, 3 = Query reservation.
'actor' : For whom to reserve/release/query ownership: 1 = GetChar, 2 = Usercode

The function will reserve or release the queue on behalf of 'actor' if it
isn't already reserved for another actor.

The function returns 1 if the queue is now reserved to 'actor', 0
otherwise.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbQueueReserve.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbQueueReserve.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbQueueReserve.m</code>
</div>
