---
layout: mfile
title: KbWait
categories:
  - PsychBasic
encoding: UTF-8
---

\[secs, keyCode, deltaSecs\] = KbWait\(\[deviceNumber\]\[, forWhat=0\]\[, untilTime=inf\]\)

Waits until any key is down and optionally returns the time in seconds
and the keyCode vector of keyboard states, just as KbCheck would do. Also
allows to wait for release of all keys or for single keystrokes, see
below.

If the optional parameter 'untilTime' is provided, KbWait will only wait
until that time and then return regardless if anything happened on the
keyboard or not.

CAUTION: KbWait periodically checks the keyboard. After each failed check
\(ie. no change in keyboard state\) it will wait for 5 msecs before the
next check. This is done to reduce the load on your system, and it is
important to do so. However if you want to measure reaction times this is
clearly not what you want, as it adds up to 5 msecs extra uncertainty to
all measurements\!

If you have trouble with KbWait always returning immediately, this could
be due to "stuck keys". See "help DisableKeysForKbCheck" on how to work
around this problem. See also "help RestrictKeysForKbCheck".

GetChar and CharAvail are character oriented \(and slow\), whereas KbCheck
and KbWait are keypress oriented \(and fast\).

Using KbWait from the MATLAB command line: When you type "KbWait" at the
prompt and hit the enter/return key to execute that command, then KbWait
will detect the enter/return key press and return immediatly.  If you
want to test KbWait from the command line, then try this:

 WaitSecs\(0.2\);KbWait

KbWait can also wait for releasing of keys instead of pressing of keys
if you set the optional 2nd argument 'forWhat' to 1.

If you want to wait for a single keystroke, set the 'forWhat' value to 2.
KbWait will then first wait until all keys are released, then for the
first keypress, then it will return. The above example could be realized
via:

 KbWait\(\[\], 2\);

If you would set 'forWhat' to 3 then it would wait for releasing the key
after pressing it againg, ie. waitForAllKeysReleased -\> waitForKeypress
-\> waitForAllKeysReleased -\> Return \[secs, keyCode\] of the key press.


# OSX and Linux

KbWait uses the PsychHID function, a general purpose function for
reading from the Human Interface Device \(HID\) class of USB devices.

KbWait tests the first USB-HID keyboard device by default. Optionally
you can pass in a 'deviceNumber' to test a different keyboard if multiple
keyboards are connected to your machine.  If deviceNumber is -1, all
keyboard devices will be checked.  If deviceNumber is -2, all keypad
devices \(if any\) will be checked. If deviceNumber is -3, all keyboard and
keypad devices will be checked. The device numbers to be checked are
determined only on the first call to the function.  If these numbers
change, the function can be reset using "clear KbWait".

As a little bonus, KbWait can also query other HID human input devices
which have keys or buttons as if they were keyboards. If you pass in the
deviceIndex of a mouse \(GetMouseIndices will provide with them\), it will
treat mouse button state as keyboard state. Similar behaviour usually
works with Joysticks, Gamepads and other input controllers.
----

See also: KbCheck, KbStrokeWait, KbPressWait, KbReleaseWait, GetChar, CharAvail, KbDemo.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbWait.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbWait.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbWait.m</code>
</div>
