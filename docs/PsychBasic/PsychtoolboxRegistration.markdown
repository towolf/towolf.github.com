---
layout: mfile
title: PsychtoolboxRegistration
categories:
  - PsychBasic
encoding: UTF-8
---

PsychtoolboxRegistration(isUpdate, flavor) - Online registration.

This function is used to register your working copy of Psychtoolbox
with the official www.psychtoolbox.org website. The routine is
normally called by PsychtoolboxPostInstallRoutine at the end of
each successfull update or initial download of a copy of Psychtoolbox.

The routine is fail-safe in the sense that it will not prevent you
from running PTB if online registration fails for some reason.

The routine transmits a bit of information about your copy of PTB and
your system environment to the website, together with a world-wide unique
identifier of your computer+operating system. The unique identifier is
the MAC address of your computers primary network adapter. We need this
to disambiguate multiple downloads/updates from the same user so we
do not count the same system setup multiple times in our statistics.
We have no way to easily find out who you are based on this information and
could not care less about that information.

# We collect this information exclusively for the following purpose:

\1. Statistics about total number of downloads for the purpose of
   documenting the use of PTB.

\2. Statistics about distribution of user base wrt. operating system,
   and Matlab / Octave version to prioritize development for the most
   common platform+OS combinations.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/PsychtoolboxRegistration.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/PsychtoolboxRegistration.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/PsychtoolboxRegistration.m</code>
</div>
