---
layout: mfile
title: FlushCalFile
categories:
  - PsychCal
encoding: UTF-8
---

FlushCalFile([filespec],[nKeep])

Flush all but the most recent calibrations in a file.

If no filespec is given, flushes file default.mat.  If
a an integer is given, flushes file screenN.mat.  If
a string is given, loads from string.mat.

Argument nKeep specifies how many calibrations to
keep.  If fewer than nKeep are in the file, all are
kept.  If nKeep is zero, file is emptied.  nKeep
defaults to 1.

If specified file cannot be found does nothing.

8/26/97  dhb  Wrote it.
8/21/00  dhb  Update for dual cal dir scheme.  Not tested hard.