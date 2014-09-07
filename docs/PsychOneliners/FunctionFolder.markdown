---
layout: mfile
title: FunctionFolder
categories:
  - PsychOneliners
encoding: UTF-8
---

filePath=FunctionFolder(functionName)

Accepts the name of a function and returns the fullpath to its enclosing
folder.  The path is the same as that returned by MATLAB's which command,
minus the name of the function itself.