---
layout: mfile
title: iViewX
categories:
  - iViewXToolbox
encoding: UTF-8
---

USAGE: [result, ivx]=iViewX(cstr, ivx [, params])

iViewX requires as input:
1\. a command string
2\. a structure with iViewX default values.
cstr:  command to execute
ivx: structure holding default information
params: optional parameters to pass on with the command

returns:
result: any result produced by the command
ivx: structure with default information (that may have been modified)