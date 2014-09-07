---
layout: mfile
title: psychrethrow
categories:
  - PsychBasic
encoding: UTF-8
---

[psychrethrow](/docs/psychrethrow)(msg) - Replacement for Matlab 6.5s builtin rethrow().
This is hopefully useful for older Matlab installations and
for the Octave port:

If the rethrow-function is supported as builtin function on
your Matlab installation, this function will call the builtin
"real" rethrow function.

If your Matlab lacks a rethrow-function, this function
will try to emulate the real rethrow function.