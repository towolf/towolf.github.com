---
layout: mfile
title: psychusejava
categories:
  - PsychJava
encoding: UTF-8
---

rc = psychusejava(level) -- Psychtoolbox wrapper for usejava
When running under a Matlab with support for the function 'usejava', we
simply invoke that function and return its result.
When running under a Matlab without that function or on Octave, we return
zero.

Drop in replacement for Matlabs usejava function.