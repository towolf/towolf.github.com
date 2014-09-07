---
layout: mfile
title: RestoreCluts
categories:
  - PsychOneliners
encoding: UTF-8
---

RestoreCluts

Restores the original CLUT's (aka gamma tables) in all graphics cards
from backup copies made during calls to LoadIdentityClut() or
BackupCluts(). This is mostly meant to undo changes made when operating
high precision display devices and similar equipment.

This is a no-operation if there aren't any CLUT's to restore.
