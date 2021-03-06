---
layout: mfile
title: CharAvail
categories:
  - PsychBasic
encoding: UTF-8
---

[avail, numChars] = CharAvail

CharAvail returns the availability of characters in the keyboard event
queue and sometimes the queue's current size. "avail" will be 1 if
characters are available, 0 otherwise.  "numChars" may hold the current
number of characters in the event queue, but in some system
configurations it is just empty, so do not rely on numChars providing
meaningful results, unless you've tested it on your specific setup.

Please read the 'help ListenChar' carefully to understand various
limitations and caveats of this function, and to learn about - often
better - alternatives.

Note that this routine does not actually remove characters from the event
queue. Call GetChar to remove characters from the queue.

GetChar and CharAvail are character-oriented (and slow), whereas KbCheck
and KbWait are keypress-oriented (and fast). See KbCheck.

See also: GetChar, ListenChar, FlushEvents, KbCheck, KbWait, KbDemo,
KbQueueDemo.