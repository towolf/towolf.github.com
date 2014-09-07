---
layout: mfile
title: SetMouse
categories:
  - PsychBasic
encoding: UTF-8
---

 SetMouse\(x, y \[, windowPtrOrScreenNumber\]\[, mouseid\]\)

 Position the mouse cursor on the screen.

 The cursor position \(x,y\) is "local", i.e. relative to the origin of the
 window or screen, if supplied. Otherwise it's "global", i.e. relative to
 the origin of the main screen \(the one with the menu bar\).

 On Linux, the optional 'mouseid' parameter allows to select which
 of potentially multiple cursors should be repositioned. On OS/X and
 Windows this parameter is silently ignored.

#  OS 9

 After calling SetMouse, there's a short period \(until the next tick?\)
 during which GetMouse reports the old position, after which it reports
 the new position. To be conservative, you can code as follows:
  while 1
    SetMouse\(theX,theY\);
    \[checkX,checkY\] = GetMouse;
    if \(checkX==theX\) && \(checkY==theY\)
       break;
    end
  end

 Cursor updating is usually carried out by a System task that runs once
 per tick, so it's likely that SetMouse doesn't take effect until the
 next tick. Instead of the elaborate check suggested above, it might
 be enough, after calling SetMouse, to simply WaitTicks\(1\) before calling
 GetMouse to be sure of getting the new position.

#  OS-X, Linux & WINDOWS

 Psychtoolbox will accept the optional windowPtrOrScreenNumber
 argument and check it for validity.  However, supplying the argument will
 not  influence the position of the mouse cursor.  The cursor is always
 positioned  in absolute coordinates on the main screen.  It does not
 matter that the  cursor is always positioned in absolute coordinates,
 because in Windows  onscreen windows are always the full size of the
 display, absolute and relative coordinates are always the same.  It would
 be good if SetMouse could position the mouse cursor on secondary
 displays, but we dont' support  multiple displays yet in Windows.

 The delay between a call to SetMouse and when GetMouse will report the
 new mouse cursor position is not known.  GetMouse seems to report the new
 position immediately, but we have no guarantee that it always will.
----

 See Also: GetMouse, GetClicks


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/SetMouse.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/SetMouse.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/SetMouse.m</code>
</div>
