---
layout: mfile
title: KbCheck
categories:
  - PsychBasic
encoding: UTF-8
---

[keyIsDown, secs, keyCode, deltaSecs] = KbCheck([deviceNumber])

Return keyboard status (keyIsDown), time (secs) of the status check, and
keyboard scan code (keyCode).

   keyIsDown      1 if any key, including modifiers such as \<shift\>,
                  \<control\> or \<caps lock\> is down. 0 otherwise.

   secs           Time of keypress as returned by GetSecs.

   keyCode        A 256-element logical array.  Each bit
                  within the logical array represents one keyboard key.
                  If a key is pressed, its bit is set, othewise the bit
                  is clear. To convert a keyCode to a vector of key
                  numbers use FIND(keyCode). To find a key's keyNumber
                  use KbName or KbDemo.

   deltaSecs      Time in seconds since this KbCheck query and the most
                  recent previous query (if any). This value is in some
                  sense a confidence interval, e.g., for reaction time
                  measurements. If KbCheck returns the information that a
                  key is pressed by the subject, then the subject could
                  have pressed the key down anytime between this
                  invocation of KbCheck at time 'secs' and the most
                  recent previous invocation. Therefore, 'deltaSecs'
                  tells you about the interval in which depression of the
                  key(s) might have happened: [secs - deltaSecs; secs].
                  for practical purpose this means that "measured" RT's
                  can't be more accurate than 'deltaSecs' seconds - the
                  interval between the two most recent keyboard checks.
                  Please note however, that standard computer keyboards
                  can incur additional delays and timing uncertainty of
                  up to 50 msecs, so the real uncertainty can be higher
                  than 'deltaSecs' -- 'deltaSecs' is just a lower bound!

KbCheck and KbWait determine whether any key is down now, including the
meta keys: \<caps lock\>, \<shift\>, \<command\>, \<control\>, and \<option\>. The
only key not reported is the start key (triangle) used to power on your
computer.

Some users of Laptops experienced the problem of "stuck keys": Some keys
are always reported as "down", so KbWait returns immediately and KbCheck
always reports keyIsDown == 1. This is often due to special function keys.
These keys or system functionality are assigned vendor specific
key codes, e.g., the status of the Laptop lid (opened/closed) could be
reported by some special keycode. Whenever the Laptop lid is open, this key
will be reported as pressed. You can work around this problem by passing
a list of keycodes to be ignored by KbCheck and KbWait. See
"help DisableKeysForKbCheck" on how to do this.

Keys pressed by the subject often show up in the Matlab command window as
well, cluttering that window with useless character junk. You can prevent
this from happening by disabling keyboard input to Matlab: Add a
ListenChar(2); command at the beginning of your script and a
ListenChar(0); to the end of your script to enable/disable transmission of
keypresses to Matlab. If your script should abort and your keyboard is
dead, press CTRL+C to reenable keyboard input -- It is the same as
ListenChar(0). See 'help ListenChar' for more info.

GetChar and CharAvail are character-oriented (and slow), whereas KbCheck
and KbWait are keypress-oriented (and fast). If only a meta key was hit,
KbCheck will return true, because a key was pressed, but CharAvail will
return false, because no character was generated. See GetChar.

KbCheck and KbWait are MEX files, which take time to load when they're
first called. They'll then stay loaded until you flush them (e.g. by
changing directory or calling CLEAR MEX).

# OSX, Linux, and Windows with Octave or Matlab R2007a and later

KbCheck uses the PsychHID function, a general purpose function for
reading from the Human Interface Device (HID) class of USB devices.

KbCheck queries the first USB-HID keyboard device by default. Optionally,
when multiple keyboards are attached to your machine, you can pass in a
'deviceNumber':  When 'deviceNumber' is -1, KbCheck will query all
keyboard devices and return their "merged state" - The 'keyCode' vector
will represent the state of all keys of all keyboards, and the
'keyIsDown' flag will be equal to one if at least one key on any of the
keyboards is pressed. When 'deviceNumber' is -2, KbCheck will query all
keypad devices (if any) and return their "merged state", and when
'deviceNumber' is -3, KbCheck will query all keyboard and keypad devices
and return their "merged state". When 'deviceNumber' is greater than 0, it
will query only the specified HID keyboard device corresponding to that
'deviceNumber'. The function GetKeyboardIndices() allows to query the
device numbers of all attached keyboards, or keyboards matching specific
criteria, and the function GetKeypadIndices() allows the same for keypads.

On MS-Windows 2000 and earlier, KbCheck can address individual keyboards.
On Windows-XP and later, it can't.

As a little bonus, KbCheck can also query other HID human input devices
which have keys or buttons as if they were keyboards. If you pass in the
deviceIndex of a mouse (GetMouseIndices will provide with them), it will
report mouse button state as keyboard state. Similar behaviour usually
works with Joysticks, Gamepads and other input controllers.
----

See also: FlushEvents, KbName, KbDemo, KbWait, GetChar, CharAvail.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbCheck.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbCheck.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbCheck.m</code>
</div>
