---
layout: mfile
title: GraphicsDisplaySyncAcrossDualHeadsTestLinux
categories:
  - PsychTests
encoding: UTF-8
---

GraphicsDisplaySyncAcrossDualHeadsTestLinux([screenids][, nrtrials=6000][, syncmethod=0])

Test synchronizity between the scanout/refresh cycles of the first two
display heads on screen 'screenids'. If 'screenids' is omitted, we test the
two heads on the screen with maximal id. 'nrtrial' sample passes
with a sampling interval of roughly 1 msecs are conducted. 'nrtrials'
defaults to 6000 samples.

Each sample consists of querying the current rasterbeam position on each
display head. At the end, the samples of both heads are plotted against each
other for comparison.

The optional parameter 'syncmethod' if set to 1 will try to synchronize all
display heads on AMD graphics cards, provided the 'ScreenToHead' mapping
(see [Screen](/docs/Screen)('[Preference](/docs/Preference)','ScreenToHead',...); is set up properly for your setup.
On a single x-screen setup this will always be the case, whereas on a multi
x-screen setup tweaking will often be required.

A 'syncmethod' of 2 is also implemented for non-AMD graphics cards, but this
implementation is so experimental that it is guaranteed to fail miserably in
practice, so don't bother trying.

The help text printed to the command window tells you how to interpret the plots.