---
layout: mfile
title: MacModelName
categories:
  - PsychOneliners
encoding: UTF-8
---

modelName=MacModelName
Return the model name of the Macintosh.

OSX: Get the computer identifier as reported by open firmware.  In the
OSX Psychtoolbox that is provided in the struct returned by
[Screen](/docs/Screen)('Computer'). Convert that identifier to Apple's marketing
name for the computer.  To do that we use the mapping of identifier to
product names found in:
/System/Library/SystemProfiler/SPPlatformReporter.spreporter/Contents/
 Resources/English.lproj/Localizable.strings.
There is no official Apple-recommended way to uncover the marketing
name. However, this method works and should be reasonably robust.

See also: [Gestalt](/docs/Gestalt), [Screen](/docs/Screen)('Computer?'), [OSName](/docs/OSName), AppleVersion