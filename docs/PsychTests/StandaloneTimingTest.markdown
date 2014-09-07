---
layout: mfile
title: StandaloneTimingTest
categories:
  - PsychTests
encoding: UTF-8
---

StandaloneTimingTest(use\_sigsetjmp, savemask)

run a timing loop in a separate process, indepenent of MATLAB.  plot the results.

use\_sigsetmask specifies whether the StandaloneTimingTest program will
call sigsetjmp() within the timing loop.  If sigsetmask is set, then
StandaloneTimingTest passes savemask to sigsetjmp in the second argument.

comparing results of TestStandaloneTimingOSX with and without
sigsetjmp shows that calling sigsetjmp with the savemask
argument set causes OS X to suspend execution of the StandaloneTimingTest
application for up to 13 ms.

SEE ALSO: StandaloneTimingTest.c