---
layout: mfile
title: KbEventFlush
categories:
  - PsychBasic
encoding: UTF-8
---

nflushed = KbEventFlush([deviceIndex])

Flush event buffer of a keyboard queue. This removes all stored events
from the keyboard event buffer of a given keyboard queue. It returns the
number of removed events in the optional return argument 'nflushed'.

By default, the event buffer of the default keyboard queue is emptied,
but you can specify 'deviceIndex' to flush the buffer of the queue
associated with 'deviceIndex'.

Keyboard event buffers are a different way to access the information
collected by keyboard queues. Before you can use an event buffer you
always must create its "parent keyboard queue" via KbQueueCreate() and
call KbQueueStart() to enable key event recording. See "help
KbQueueCreate" etc. on how to do this.
----

See also: KbQueueCreate, KbQueueStart, KbQueueStop, KbQueueCheck,
           KbQueueWait, KbQueueFlush, KbQueueRelease