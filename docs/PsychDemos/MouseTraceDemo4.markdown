---
layout: mfile
title: MouseTraceDemo4
categories:
  - PsychDemos
encoding: UTF-8
---

MouseTraceDemo4
----

Draw a curve with the mouse. Same as MouseTraceDemo, but asks
[Screen](/docs/Screen)('[Flip](/docs/Flip)') to not clear the framebuffer after flip. This way,
we don't need to redraw the whole mouse trace in each frame.
Uses imaging pipeline via PsychImaging for optimal performance
on modern hardware, as opposed to old style method shown in
MouseTraceDemo2, which was appropriate before the year 2007.
----

See also: PsychDemos, MouseTraceDemo, GetMouse.

# HISTORY

4/1/2013  mk       Derived from MouseTraceDemo2.