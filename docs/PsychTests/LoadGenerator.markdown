---
layout: mfile
title: LoadGenerator
categories:
  - PsychTests
encoding: UTF-8
---

LoadGenerator([yieldmsecs=0])

Create cpu-load by simply executing an empty while-loop as fast as
possible.

Optionally the load can be reduced by specifying a non-zero 'yieldmsecs'
argument telling the function that it should release the cpu for
'yieldmsecs' milliseconds in each loop iteration.

This function never returns, you have to abort it by pressing CTRL+C.
