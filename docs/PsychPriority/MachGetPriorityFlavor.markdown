---
layout: mfile
title: MachGetPriorityFlavor
categories:
  - PsychPriority
encoding: UTF-8
---

# OS X

MachGetPriorityFlavor returns the priority flavor mode of the main
MATLAB thread, either 'THREAD\_TIME\_CONSTRAINT\_POLICY' or
'THREAD\_STANDARD\_POLICY'.

The second return argument, priorityStruct, is the  priority struct for
the active priority flavor mode.

The priority flavor 'THREAD\_PRECEDENCE\_POLICY' is never returned
because its status is implied  by either 'THREAD\_TIME\_CONSTRAINT\_POLICY'
or  'THREAD\_STANDARD\_POLICY':

  -If flavorNameString is 'THREAD\_TIME\_CONSTRAINT\_POLICY', then then
  'THREAD\_PRECEDENCE\_POLICY'and its 'importance' parameter  are ignored
  by the Mach task scheduler.

  -If flavorNameString is 'THREAD\_STANDARD\_POLICY' then the 'importance'
  parameter associated with 'THREAD\_PRECEDENCE\_POLICY' governs the
  relative allocation of CPU time between the main MATLAB thread and all
  other threads of the MATLAB process.

MachGetPriorityFlavor probes priority using MachGetPriorityMex.

# OS 9

MachGetPriorityFlavor does not exist in OS 9.

# WINDOWS

MachGetPriorityFlavor does not exist in Windows.
----

see also: [Priority](/docs/Priority), [Rush](/docs/Rush), MachGetPriorityMex, MachSetPriorityMex,