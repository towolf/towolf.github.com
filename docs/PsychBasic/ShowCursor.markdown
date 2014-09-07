---
layout: mfile
title: ShowCursor
categories:
  - PsychBasic
encoding: UTF-8
---

oldType = ShowCursor\(\[type\] \[, screenid\]\[, mouseid\]\)

ShowCursor redisplays the mouse pointer after a previous call to
HideCursor. If the optional 'type' is specified, it also allows to alter
the shape of the cursor. See following sections for details.

The optional 'mouseid' allows to select which mouse cursor shall
be redisplayed or changed in visual appearance. This only makes sense
if you have multiple visible mouse cursors and is currently a Linux only
feature.

The return value 'oldType' is always zero, as this query mechanism is not
supported with PTB-3. Just returned for backwards-compatibility.

# OSX, WINDOWS, LINUX

# Cursor shape can be selected. Four types are defined by name:

'Arrow' = Standard mouse-pointer arrow.
'CrossHair' = A cross-hair cursor.
'Hand' = A hand symbol.
'SandClock' = Some sort of sand clock/hour-glass \(not available on 64-Bit OSX\).

 Apart from that names, you can pass integral numbers for type to select
 further shapes. The mapping of numbers to shapes is operating system
 dependent, therefore not portable across different platforms. On
 MS-Windows, you can select between number 0 to 7. On Linux/X11 you can
 select from a wide range of numbers from 0 up to \(at least\) 152, maybe
 more, depending on your setup. See the C header file "X11/cursorfont.h"
 for a mapping of numbers to shapes. Passing invalid numbers can create
 errors. On 32-Bit OS/X, numbers between zero and 17 are currently valid.
 You can find a list of mappings from type to number for 32-Bit OS/X at:
 http://developer.apple.com/documentation/macos8/HumanInterfaceToolbox/Ap
 pManager/ProgWithAppearanceMgr/Appearance.9d.html\#10244

# LINUX

Linux allows for display and handling of multiple mouse cursors if your
X-Server is of version 1.7 or later.

If provided, the optional "type" argument changes the cursor shape to:
  0: Arrow
  1: I Beam
  2: Cross
  3: Plus
  4: Watch
  5: Arrow
128: P
300: Beachball 1/4
301: Beachball 2/4
302: Beachball 3/4
303: Beachball 4/4
400: fat arrow
401: fat I Beam
Type 0 \(and 5 for backward compatibility\) is predefined as the standard
arrow cursor. The rest return whatever Apple's GetCursor\(type\) finds in
the  System or Matlab's resource forks. If nothing is found, the type is
reset to 0. The fat arrow and I beam are copied from the "Fat Cursors v
1.2" control panel created by Robert Abatecola, 5106 Forest Glen Drive,
San Jose, CA 95129.
----


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/ShowCursor.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/ShowCursor.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/ShowCursor.m</code>
</div>
