---
layout: mfile
title: BackupCluts
categories:
  - PsychOneliners
---

Backup current clut gamma tables of screens for later restoration via RestoreCluts\(\).

# Usage:

BackupCluts\(\[screenIds=all\]\);

Saves all cluts/gamma tables of all connected display screens by default,
or of specified vector 'screenIds' to a global variable. The cluts can be
restored from this backup copy by simply calling "RestoreCluts". This is
also done automatically if "[sca](/docs/sca)" is executed at the end of a session.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/BackupCluts.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/BackupCluts.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/BackupCluts.m</code>
</div>
