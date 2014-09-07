---
layout: mfile
title: GetProcessDescriptorFromCommandName
categories:
  - PsychPriority
encoding: UTF-8
---

processDescriptor=GetProcessDescriptorFromCommandName\(commandName\)

OS X: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Accept the name of a process and return a structure with fields
describing that process.  GetProcessDescriptorFromCommandName relies on
the Unix command "ps" to get information about processes.

# Try:

  GetProcessDescriptorFromCommandName\('MATLAB'\);

OS 9: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

GetProcessDescriptorFromCommandName does not exist in OS 9.

WINDOWS: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

GetProcessDescriptorFromCommandName does not exist in Windows.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

SEE ALSO: GetProcessList, GetRawProcessList


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychPriority/GetProcessDescriptorFromCommandName.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychPriority/GetProcessDescriptorFromCommandName.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychPriority/GetProcessDescriptorFromCommandName.m</code>
</div>
