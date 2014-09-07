---
layout: mfile
title: GraphicsDisplaySyncAcrossDualHeadsTest
categories:
  - PsychTests
encoding: UTF-8
---

GraphicsDisplaySyncAcrossDualHeadsTest([screenids] [, nrtrials=6000] [, driftsync=0])

Test synchronizity between the scanout/refresh cycles of two different
display heads 'screenids(1)' and 'screenids(2)'. If 'screenids' is
omitted, we test the two heads with maximal id. 'nrtrial' sample passes
with a sampling interval of roughly 1 msecs are conducted. 'nrtrials'
defaults to 6000 samples.

Each sample consists of querying the current rasterbeam position and
timestamp of last VBL interrupt on each display head. At the end, the
samples of both heads are plotted against each other and compared.

The help text in the Matlab prompt tells you how to interpret the plots.