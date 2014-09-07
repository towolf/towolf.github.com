---
layout: mfile
title: AppleVersion
categories:
  - PsychOneliners
---

versionString=AppleVersion\(gestaltString\)

OS 9 and OS X: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

AppleVersion\('qtim'\) % QuickTime
AppleVersion\('atkv'\) % AppleTalk
Uses [Gestalt](/docs/Gestalt) to retrieve Apple version information and returns a string.
Apple has a "standard" format for versions, e.g. 3.0f7 or 8.0.1, that
they use for some of their software components. APPLEVERSION uses GESTALT
to retrieve the information. However, this is only useful for the few
[Gestalt](/docs/Gestalt) selectors that return information in this "standard" format.
If the selector is undefined \(possibly because that software is
not present\) APPLEVERSION returns an empty string.

WINDOWS: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

AppleVersion does not exist in Windows.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

see also: [Gestalt](/docs/Gestalt), [Screen](/docs/Screen)\('Computer?'\), MacModelName


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/AppleVersion.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/AppleVersion.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/AppleVersion.m</code>
</div>