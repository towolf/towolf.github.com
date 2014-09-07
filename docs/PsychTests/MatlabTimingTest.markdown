---
layout: mfile
title: MatlabTimingTest
categories:
  - PsychTests
encoding: UTF-8
---

MatlabTimingTest

Assign the main MATLAB thread "time constraint" priority status and
run a tight loop which records with high preceision the time at every
pass through the loop.  Calculate the time intervals between succussive
passes through the loop.

Granting MATLAB "time constraint" priority prevents any other thread on the
system from preempting the main MATLAB thread. Other threads recieve
CPU time only at the discretion of the main MATLAB thread which executes
your MATLAB scripts and functions.  Therefore, the delay between
the nth and the (n+1)th timing loop is not caused by other threads
preempting MATLAB, but instead by some activity of MATLAB itself or the script which it executes.

MatlabTimingTest samples the time using GetSecsMex, a custom mex file
which calls the native OSX Core Audio function AudioGetCurrentHostTime()
The precision depends on the CPU and clocks speed, on a 1GHZ G4 clock tick
period is 30 nanoseconds)

AUTHORS: Allen Ingling
SEE ALSO: GetSecsMex