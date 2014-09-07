---
layout: mfile
title: PsychJavaSwingCleanup
categories:
  - PsychJava
encoding: UTF-8
---

PsychJavaSwingCleanup - Clean up some internal Java stuff.

The Matlab GUI is based on Java Swing, which occasionly causes problems
when used with Psychtoolbox due to internal quirks of Swing's
RepaintManager class ("OutOfMemoryError in Java heap space").
PsychJavaSwingCleanup() forces the RepaintManager to re-initialize by
temporarily setting its screen buffer to zero size. Calling the garbage
collector is probably not really necessary because it gets called by
Matlab at some point anyway. Finally we try to overcome the problem that
the RepaintManager apparently forgets about its dirty regions while
re-initializing.

This routine is closely derived from the one posted in Psychtoolbox forum
message #16043 by user qx1147.

Another possible solution is described and offered in message #13975 by
Davide Tabarelli.
