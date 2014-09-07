---
layout: mfile
title: MachAbsoluteTimeClockFrequency
categories:
  - PsychBasic
encoding: UTF-8
---

timebaseFrequencyHz = MachAbsoluteTimeClockFrequency

# OS X

Return the frequency of the Mach Kernel "absolute timebase clock".  The
frequency depends your  hardware, both the model of CPU and a system
hardware clock.

Mach Kernel functions which assign real-time "Time constraint priority"
status to threads give parameters in Mach time base units. The counter which
clocks time allocated to your thread counts time in these units.  Use the
absolute timebase clock frequency returned by MachAbsoluteTimeClockFrequency to convert
seconds into absolute timebase units which you pass to functions which
set which set priority:

  time\_interval\_in\_mach\_units=
       time\_interval\_in\_seconds \* timebaseFrequencyHz;

For more information on the Mach absolute time clock see Apple Technical
Q&A 1398:

 http://developer.apple.com/qa/qa2004/qa1398.html

# OS 9

MachAbsoluteTimeClockFrequency is not provided on OS 9 because the Mach
time base is a feature of only the OS X Mach Kernel.


# WINDOWS

MachAbsoluteTimeClockFrequency is not provided on Windows because the
Mach time base is a feature of only the OS X Mach Kernel.
----

see also: [Priority](/docs/Priority)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/MachAbsoluteTimeClockFrequency.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/MachAbsoluteTimeClockFrequency.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/MachAbsoluteTimeClockFrequency.m</code>
</div>
