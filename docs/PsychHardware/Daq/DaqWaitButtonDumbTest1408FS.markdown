---
layout: mfile
title: DaqWaitButtonDumbTest1408FS
categories:
  - Daq
encoding: UTF-8
---

DaqWaitButtonDumbTest1408FS.m

A quick and dirty demo on how to poll the digital inputs
of a USB-1408FS as fast as possible, without overhead.

This is essentially a stripped down version of DaqDIn() with
some polling loops wrapped around and a options.secs value of
zero for essentially polling with no timeout.
