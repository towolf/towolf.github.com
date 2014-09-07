---
layout: mfile
title: DoNothing
categories:
  - PsychBasic
encoding: UTF-8
---

function [empty1,etc]=DoNothing([arg1],[etc])

DoNothing is a dummy MEX routine used to measure Matlab's overhead
in calling MEX functions. Input arguments are ignored. DoNothing
returns an empty matrix for each explicitly provided output argument.