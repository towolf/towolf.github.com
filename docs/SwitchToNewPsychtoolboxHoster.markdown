---
layout: mfile
title: SwitchToNewPsychtoolboxHoster
categories:
  - .
encoding: UTF-8
---

Switch a installed Psychtoolbox working copy to our new host GoogleCode.

This function checks if the currently installed Psychtoolbox working copy
is still attached to Berlios code hosting. If so, it tries to switch it
over to our new code hosting provider GoogleCode. Otherwise it does
nothing.

This function is called by the PsychtoolboxPostInstallRoutine after each
invocation of DownloadPsychtoolbox, UpdatePsychtoolbox or SetupPsychtoolbox.
It takes care of the transition.

The function can also be called manually by users in the year 2012 and
later, when the standard installation and update routines do no longer
work due to Berlios servers being offline.
