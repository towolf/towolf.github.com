---
layout: mfile
title: KbStrokeWait
categories:
  - PsychBasic
encoding: UTF-8
---

[secs, keyCode, deltaSecs] = KbStrokeWait([deviceNumber][, untilTime=inf][, more optional args for KbWait]);

KbStrokeWait waits for a single keystroke of your subject, ie. it waits
until all keys on the keyboard are released, after that it waits for a
single keystroke - a single press of a key, followed by releasing the key
again. After the subject has finished its "keystroke" and released the key,
KbStrokeWait returns the keyboard state and timestamp of the key press.

It also returns if the optional deadline 'untilTime' is reached.

This is a convenience wrapper, doing the same thing as
KbWait(deviceNumber, 3, ...); so read "help KbWait" for details about
operation and returned values.

You'll typically use this function to ask your subject for input of a
single character, or for confirmation of something (e.g., "Press any key
when you're ready for the next block of trials").

See also: KbPressWait, KbReleaseWait, KbWait, KbCheck, KbStrokeWait.