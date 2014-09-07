---
layout: mfile
title: PR705write
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705write - Write a string of characters to the PR-705.

Syntax:
varargout = PR705write(cmdStr [, block=1])

Description:
This is a convenience wrapper to write data to the PR-705 device. Aside
from appending a carriage return and not requiring an explicit port
handle, this function is identical to [IOPort](/docs/IOPort)'s Write (see [IOPort](/docs/IOPort) Write?
for more details).

Inputs:
datastr (1xN char) - data string to write to the PR-705.
block (scalar) - enable (1, default) or disable (0) blocking writes

Outputs:
Refer to [IOPort](/docs/IOPort) Write?

11/29/12    zlb   Wrote it.