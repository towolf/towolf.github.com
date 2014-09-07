---
layout: mfile
title: OSName
categories:
  - PsychOneliners
encoding: UTF-8
---

sysNameStr = [OSName](/docs/OSName)

Return the convential English-language name for your operating system (OS).
[OSName](/docs/OSName) is useful in constructing error message strings which refer to
particular operating systems. System name strings as returned by the MATLAB
command "computer" are unsuitable for this purpose because they are
abbreviations, not names.

Currently possible returned namestrings are 'Windows', 'Linux' or 'OSX'.

see also: computer, IsOSX, IsWin, IsLinux, MacModelName, DescribeComputer