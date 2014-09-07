---
layout: mfile
title: AddPsychJavaPath
categories:
  - PsychJava
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


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychJava/AddPsychJavaPath.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychJava/AddPsychJavaPath.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychJava/AddPsychJavaPath.m</code>
</div>
