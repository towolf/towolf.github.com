---
layout: mfile
title: ISO2007MPEBasicTest
categories:
  - PsychISO2007MPE
encoding: UTF-8
---

ISO2007MPEBasicTest

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the ISO2007MPE routines, please see the notes on usage
and responsibility in PsychISO2007MPE/Contents.m (type "help PsychISO2007MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Test code for our implementation of the ISO 2007 broadband MPE standard.

We don't have any known test cases to check, particularly since we can
only measure light in the visible.  Here we verify that a bright sunlight
measured in Philly is below the MPE, but not by all that much.  This is
broadly consistent with what we find when we compare the same light to the ANSI
standard for laser light (with a few assumptions to apply that standard to
broadband light.)

6/26/13  dhb  Wrote it.