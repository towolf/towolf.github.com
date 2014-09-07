---
layout: mfile
title: KbQueueDemo
categories:
  - PsychDemos
encoding: UTF-8
---

KbQueueDemo([deviceIndex])
Shows how to detect when the user has pressed a key.
See KbQueueCheck, KbQueueWait, KbName, KbCheck, KbWait, GetChar, CharAvail.

The KbQueueXXX functions are low-level like KbCheck and KbWait, but, like
GetChar/CharAvail, they use a queue so that brief events can be captured.

Like GetChar/CharAvail, KbQueueXXX functions may be used
asychronously - the OS will pick up the character whether your code
is currently looking for it or not so long as the queue has already been
created(using KbQueueCreate) and started (using KbQueueStart).

Unlike GetChar/CharAvail, KbQueueXXX functions can detect isolated presses
of modifier keys. Also, the times of key presses should be more accurate than
those associated with GetChar/CharAvail or with KbCheck and the timebase is
the same as that returned by GetSecs (unlike GetChar/CharAvail).

The first four demos here are analogous to those in KbDemo.m