---
layout: mfile
title: glmSwapBuffers
categories:
  - wrap
encoding: UTF-8
---

glmSwapBuffers  Swap front and back buffers

usage:  [ t, w ] = glmSwapBuffers( pauseflag )

Return argument 't' is the absolute time at which the call to
aglSwapBuffers() returned, and 'w' is the time that aglSwapBuffers()
took to return, i.e., the time spent waiting for a vertical retrace.
These values are useful for checking video timing.