---
layout: mfile
title: DaqtoolboxConfigDir
categories:
  - Daq
encoding: UTF-8
---

Syntax: AbsolutePath = DaqtoolboxConfigDir

Purpose: Look for (create if necessary) folder containing preferences for Daq
         toolbox;

History: 1/28/08  mpr configured this was needed
         3/7/08   mpr streamlined this

Function does not assume that user is using Psychophysics toolbox, but will
subordinate Daqtoolbox if that assumption is correct.  That is, function will
look for Daqtoolbox preferences in a folder containing Psychtoolbox
preferences.  It will create its own folder iff it does not find one, and that
folder will be in the Psychtoolbox preferences folder if that folder exists.