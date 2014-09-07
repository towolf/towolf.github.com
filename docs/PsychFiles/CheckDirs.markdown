---
layout: mfile
title: CheckDirs
categories:
  - PsychFiles
encoding: UTF-8
---

CheckDirs(dirs,mode):
Iterates over all fields in struct 'dirs' and checks whether the Contents are existing directory addresses.
mode == 'check': Display an error if this is not the case.
mode == 'make' : Creates the directory if it doesnt exist.
Default mode is 'check'.
JvR 2008-03-31