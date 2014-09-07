---
layout: mfile
title: FlushEvents
categories:
  - PsychBasic
encoding: UTF-8
---

FlushEvents(['mouseUp'],['mouseDown'],['keyDown'],['autoKey'],['update'],...)

Remove events from the system event queue.

Removes all events of the specified types from the event queue.
The arguments can be in any order. Empty strings are ignored.

Please read the 'help ListenChar' carefully to understand various
limitations and caveats of this function, and to learn about - often
better - alternatives.

FlushEvents will accept all arguments for backward compatibility with
Psychtoolbox-2, but only 'keyDown' (or no argument at all) removes
keypress events. Events other than keypress events are not supported.

See also: GetChar, CharAvail, FlushEvents, EventAvail.