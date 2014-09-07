---
layout: mfile
title: JavaTimeToGetSecs
categories:
  - PsychJava
---

timeSecs=JavaTimeToGetSecs\(javaTime, \[updateInterval\]\)

Convert time as reported by "java.lang.System.currentTimeMillis\(\)" to
GetSecs units.

The Java timebase and JavaTimeToGetSecs are used internally by GetChar
because Java calls underlying GetChar timestamp keyboard events in those
units.

updateInterval is the number of seconds before this function updates its
internal timing cache measuring the difference between GetSecs and
java.lang.System.currentTimeMillis\(\).  If set to \-1, the cache is only
made the first time this function funs.  When ommitted, it defaults to 0,
i.e., it recaches at every call.


see also:


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychJava/JavaTimeToGetSecs.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychJava/JavaTimeToGetSecs.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychJava/JavaTimeToGetSecs.m</code>
</div>
