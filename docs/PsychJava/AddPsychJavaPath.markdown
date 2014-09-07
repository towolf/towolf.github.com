---
layout: mfile
title: AddPsychJavaPath
categories:
  - PsychJava
encoding: UTF-8
---

Add Psychtoolbox directories containing Java classes to the path
which MATLAB searches for Java classes.  The MATLAB Java path is separate
from the path searched for .m and mex functions.

PsychtJavaPaths updates the MATLAB Java path lazily, detecting first
whether the MATLAB paths have already been changed before making changes.

AddPsychJavaPath is called by Psychtoolbox functions which depend on
Psychtoolbox Java classes; It should be unnecessary to use it within your
own programs.

see also: PsychJava, IsPsychJavaPathSet