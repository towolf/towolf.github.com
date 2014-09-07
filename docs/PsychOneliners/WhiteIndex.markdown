---
layout: mfile
title: WhiteIndex
categories:
  - PsychOneliners
encoding: UTF-8
---

color=WhiteIndex(windowPtrOrScreenNumber)
Returns the intensity value to produce white at the current screen depth,
assuming a standard color lookup table for that depth. E.g.

white=WhiteIndex(w);
[Screen](/docs/Screen)(w,'FillRect',white);

windowPtrOrScreenNumber must be a screen number or a handle for
an onscreen window. It won't work on offscreen windows or textures.

See BlackIndex.
