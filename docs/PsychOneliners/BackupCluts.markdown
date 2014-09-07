---
layout: mfile
title: BackupCluts
categories:
  - PsychOneliners
encoding: UTF-8
---

Backup current clut gamma tables of screens for later restoration via RestoreCluts().

# Usage:

BackupCluts([screenIds=all]);

Saves all cluts/gamma tables of all connected display screens by default,
or of specified vector 'screenIds' to a global variable. The cluts can be
restored from this backup copy by simply calling "RestoreCluts". This is
also done automatically if "[sca](/docs/sca)" is executed at the end of a session.
