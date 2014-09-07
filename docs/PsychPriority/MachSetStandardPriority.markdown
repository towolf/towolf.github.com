---
layout: mfile
title: MachSetStandardPriority
categories:
  - PsychPriority
encoding: UTF-8
---

MachSetStandardPriority

# OS X

Restores the standard priorty flavor THREAD\_STANDARD\_POLICY to  the main
MATLAB thread.  MachSetStandardPriority undoes previous calls to either
MachSetTimConstraintPolicy or
MachSetPriorityMex('THREAD\_TIME\_CONSTRAINT\_POLICY',...)

# OS 9

MachSetStandardPriority does not exist in OS 9.

# WINDOWS

MachSetStandardPriority does not exist in Windows.
----

see also: [Priority](/docs/Priority), [Rush](/docs/Rush), MachGetPriorityFlavor, MachSetPriorityMex,