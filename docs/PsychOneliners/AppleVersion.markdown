---
layout: mfile
title: AppleVersion
categories:
  - PsychOneliners
encoding: UTF-8
---

versionString=AppleVersion(gestaltString)

# OS 9 and OS X

AppleVersion('qtim') % QuickTime
AppleVersion('atkv') % AppleTalk
Uses [Gestalt](/docs/Gestalt) to retrieve Apple version information and returns a string.
Apple has a "standard" format for versions, e.g. 3.0f7 or 8.0.1, that
they use for some of their software components. APPLEVERSION uses GESTALT
to retrieve the information. However, this is only useful for the few
[Gestalt](/docs/Gestalt) selectors that return information in this "standard" format.
If the selector is undefined (possibly because that software is
not present) APPLEVERSION returns an empty string.

# WINDOWS

AppleVersion does not exist in Windows.
----

see also: [Gestalt](/docs/Gestalt), [Screen](/docs/Screen)('Computer?'), MacModelName