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
