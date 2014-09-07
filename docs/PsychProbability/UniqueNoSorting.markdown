---
layout: mfile
title: UniqueNoSorting
categories:
  - PsychProbability
encoding: UTF-8
---

output = UniqueNoSorting\(sequence,mode\)

SEQUENCE is a vector, MODE is a specification of how you want your output
to be not sorted.

Basically the same as unique, but returns the unique values either:
"in order of appearance"        - \(MODE = 'first' for 'first occurrence'\)
or
"in order of disappearance"     - \(MODE = 'last'  for 'last occurrence'\)

MODE defaults to 'first'

JvR 2008-05-06


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychProbability/UniqueNoSorting.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychProbability/UniqueNoSorting.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychProbability/UniqueNoSorting.m</code>
</div>
