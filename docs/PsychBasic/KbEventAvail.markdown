---
layout: mfile
title: KbEventAvail
categories:
  - PsychBasic
encoding: UTF-8
---

navail = KbEventAvail([deviceIndex])

Return current number of recorded events in the event buffer of a
keyboard queue in the return argument 'navail'.

By default, the event buffer of the default keyboard queue is checked,
but you can specify 'deviceIndex' to check the buffer of the queue
associated with 'deviceIndex'.

Keyboard event buffers are a different way to access the information
collected by keyboard queues. Before you can use an event buffer you
always must create its "parent keyboard queue" via KbQueueCreate() and
call KbQueueStart() to enable key event recording. See "help
KbQueueCreate" etc. on how to do this.
----

See also: KbQueueCreate, KbQueueStart, KbQueueStop, KbQueueCheck,
           KbQueueWait, KbQueueFlush, KbQueueRelease


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbEventAvail.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbEventAvail.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbEventAvail.m</code>
</div>
