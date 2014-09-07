---
layout: mfile
title: KbReleaseWait
categories:
  - PsychBasic
encoding: UTF-8
---

[secs, keyCode, deltaSecs] = KbReleaseWait([deviceNumber][, untilTime=inf][, more optional args for KbWait]);  

KbReleaseWait waits until all keys on the keyboard are released.  

It also returns if the optional deadline 'untilTime' is reached.  

This is a convenience wrapper, doing the same thing as  
KbWait(deviceNumber, 1, ...); so read "help KbWait" for details about  
operation and returned values.  

You'll typically use this function to make sure that all keys are idle  
before you start some new trial that collects keyboard responses, after  
you've used KbCheck, KbWait or KbPressWait for collecting a response. A  
different approach is to use KbStrokeWait.  

See also: KbPressWait, KbReleaseWait, KbWait, KbCheck, KbStrokeWait.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbReleaseWait.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbReleaseWait.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbReleaseWait.m</code>
</div>
