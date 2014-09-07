---
layout: mfile
title: LogVar
categories:
  - PsychFiles
encoding: UTF-8
---

fname = LogVar(var,name,dirnm)

Turns a variable VAR into a string that evaluates back to the original
variable, e.g. when feeding it to eval()
NAME is the name of the variable that will be used in this string
String will be saved in a text file in the directory DIRNM with as
filename the name of the variable NAME and the time at which the file is
written.

DN 2008