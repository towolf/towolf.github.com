---
layout: mfile
title: PR705read
categories:
  - PR705Toolbox
encoding: UTF-8
---

PR705read - Read data from the PR-705.

Syntax:
serialData = PR705read([block=0] [, nbytes])

Description:
This is a convenience wrapper to read data from the PR-705 device. Aside
from not requiring an explicit port handle, this function is identical to
[IOPort](/docs/IOPort)'s Read (see [IOPort](/docs/IOPort) Read? for more details).

Output:
serialData (1xN char).

11/29/12    zlb   Wrote it based on the PR670Toolbox.