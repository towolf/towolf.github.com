---
layout: mfile
title: ClutAnimDemo
categories:
  - PsychDemos
encoding: UTF-8
---

ClutAnimDemo([method=0])

Display an animated grating using CLUT animation via the
[Screen](/docs/Screen)('LoadNormalizedGammaTable') command, or via the PsychImaging()
based clut animation support.

Clut animation is an ancient technique of achieving animation, only
needed or the best choice for very few use cases nowadays. Think twice
before using this as your method of choice. It may work, but is inefficient,
potentially unreliable in the timing domain (except for method 2) and most
often more painful and inflexible to use than a proper modern approach.

If 'method' is left out or set to 0, hardware gamma tables are
immediately updated. A setting of 1 will update hardware gamma tables in
sync with [Screen](/docs/Screen)('[Flip](/docs/Flip)'), or more accurately, it will try to.
Synchronization can't be guaranteed, only that a good effort is made to
achieve sync. A 'method' setting of 2 will use the Psychtoolbox image
processing pipeline to implement clut animation, instead of updating the
hardware gamma tables. This is the only reliable method with respect to
timing precision. It is also the only method that works on MS-Windows.
However, it requires recent graphics hardware and a bit more computation
time.

Method 2 is recommended for most use cases, method 0 is the least
reliable one.

see also: PsychDemos, PsychImaging
