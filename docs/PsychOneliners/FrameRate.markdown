---
layout: mfile
title: FrameRate
categories:
  - PsychOneliners
encoding: UTF-8
---

hz=FrameRate([windowOrScreenNumber])

Returns accurate frame rate of window or screen. Default is the main
screen. The windowOrScreenNumber and frame rate are cached so subsequent
calls after the first take no time at all.
See also "[Screen](/docs/Screen) GetFlipInterval?"