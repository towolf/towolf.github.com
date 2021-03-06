---
layout: mfile
title: FlipTest
categories:
  - PsychTests
encoding: UTF-8
---

FlipTest

FlipTest times and plots the intervals between flips of the front and
back display buffers in a tight loop.  Flips should occur at the video
frame period.  Result of lipTest are a test of [Priority](/docs/Priority)'s ability to
gurantee time to MATLAB for real-time displays.

On OS X, the [Screen](/docs/Screen) subfunction '[Flip](/docs/Flip)' replaces 'WaitBlanking' as a means
of sycnrhonizing updates of video memory with the vertical retrace of your
monitor.  This prevents vertical shearing of displays.

Onscreen windows in OS X are double buffered, having two surfaces:
front and back.  The front surface is memory from which video DACs read
and is displayed on your montitor.  The back surface is video memory to
which rendering commands draw.

A call to [Screen](/docs/Screen) '[Flip](/docs/Flip)' delays until the next vertical retrace, then
instantaneously interchanges front and back video surfaces, and then
returns.