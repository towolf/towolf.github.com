---
layout: mfile
title: GetProcessDescriptorFromCommandName
categories:
  - PsychPriority
encoding: UTF-8
---

processDescriptor=GetProcessDescriptorFromCommandName(commandName)

# OS X

Accept the name of a process and return a structure with fields
describing that process.  GetProcessDescriptorFromCommandName relies on
the Unix command "ps" to get information about processes.

# Try:

  GetProcessDescriptorFromCommandName('MATLAB');

# OS 9

GetProcessDescriptorFromCommandName does not exist in OS 9.

# WINDOWS

GetProcessDescriptorFromCommandName does not exist in Windows.
----

SEE ALSO: GetProcessList, GetRawProcessList