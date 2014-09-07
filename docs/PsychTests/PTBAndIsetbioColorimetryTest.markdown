---
layout: mfile
title: PTBAndIsetbioColorimetryTest
categories:
  - PsychTests
encoding: UTF-8
---

PTBAndIsetbioColorimetryTest

This script compares values calculated by PTB and routines in isetbio (developed by
Wandell and colleague) for various colorimetric functions.

For information on isetbio, see https://github.com/wandell/vset/blob/master/README.txt.
It contains its own implementation of many of the colorimetric computations
implemented in PTB.  Note that Brainard and Wandell are not completely
independent sources.

Make sure isetbio is on your path to run these comparisons.  The tests should
also work if you have the proprietary iset on your path instead.
isetbio is available on gitHub as https://github.com/wandell/isetbio.git.

The checks are grouped into cells that check one thing at a time.

Because DHB and BAW have too much time on their hands -
 "A man with one watch always knows what time it is, a man with two is never sure."
 "A man with SPM knows how to blur and average his watches so that he can't tell the time"

7/7/10  dhb  Wrote it.
x/xx/10 baw  Checked with ISET-4.0 revision 351 (BW)
2/28/13 dhb  Updated to work with vset rather than proprietary iset.
8/5/13  dhb  Updated to work with isetbio, vset's successor.
7/31/14 dhb, ncp Put a cd around call to isetbio xyz2lab to deal with
             fact that 2014b has added a routine with this name that
             doesn't work quite the same.