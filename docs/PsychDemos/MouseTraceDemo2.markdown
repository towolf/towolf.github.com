---
layout: mfile
title: MouseTraceDemo2
categories:
  - PsychDemos
encoding: UTF-8
---

MouseTraceDemo2
----

Draw a curve with the mouse. Same as MouseTraceDemo, but asks
[Screen](/docs/Screen)('[Flip](/docs/Flip)') to not clear the framebuffer after flip. This way,
we don't need to redraw the whole mousetrace in each frame.
----

See also: PsychDemos, MouseTraceDemo, GetMouse.

# HISTORY

4/23/05  mk       Derived from MouseTraceDemoOSX: Uses new "Don't clear" mode of [Flip](/docs/Flip).
                  to avoid redrawing the whole past mousetrace after each
                  [Flip](/docs/Flip) --\> Faster.