---
layout: mfile
title: glmSetSwapInterval
categories:
  - wrap
encoding: UTF-8
---

glmSetSwapInterval  Set number of video frames between buffer flushes

usage:  glmSetSwapInterval( nframes )

Note:  The AGL documentation indicates that 'nframes' will control the
number of vertical refreshes between buffer flushes.  In practice, it seems
that nframes=0 disables vertical refresh syncing, and nframes=1 or higher
just enables it.