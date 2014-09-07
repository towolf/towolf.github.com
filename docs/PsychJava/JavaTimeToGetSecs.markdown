---
layout: mfile
title: JavaTimeToGetSecs
categories:
  - PsychJava
encoding: UTF-8
---

timeSecs=JavaTimeToGetSecs(javaTime, [updateInterval])

Convert time as reported by "java.lang.System.currentTimeMillis()" to
GetSecs units.

The Java timebase and JavaTimeToGetSecs are used internally by GetChar
because Java calls underlying GetChar timestamp keyboard events in those
units.

updateInterval is the number of seconds before this function updates its
internal timing cache measuring the difference between GetSecs and
java.lang.System.currentTimeMillis().  If set to -1, the cache is only
made the first time this function funs.  When ommitted, it defaults to 0,
i.e., it recaches at every call.


see also: