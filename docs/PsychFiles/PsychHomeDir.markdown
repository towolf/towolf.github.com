---
layout: mfile
title: PsychHomeDir
categories:
  - PsychFiles
encoding: UTF-8
---

Purpose: Look for the home directory of the user.

Syntax: path=PsychHomeDir([subDir])

         When called without optional 'subDir' argument, the path to the
         users home folder is returned. When 'subDir' is given, the
         path to the subfolder 'subDir' inside the home folder
         is returned - and the 'subDir' created inside that folder
         if neccessary.

History: 1/23/08    mpr configured it was about time to write this
         3/7/08     mpr streamlined this
         3/8/08     mk  A bit more of streamlining - Don't write the
                        PsychPrefsfolder.m file anymore.
         4/28/08    mk  Made compatible with Octave, added 'subDir'
                        option.
         2/06/09    mk  Derived from PsychtoolboxConfigDir().