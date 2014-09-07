---
layout: mfile
title: ListenChar
categories:
  - PsychBasic
encoding: UTF-8
---

function ListenChar\(\[listenFlag\]\)

Tell the Psychtoolbox function "GetChar" to start or stop listening for
keyboard input.  By default ListenChar listens when no argument is
supplied.  Passing 0 will turn off character listening and reset the
buffer which holds the captured characters. Passing a value of 1 or not
passing any value will enable listening. Passing a value of 2 will enable
listening, additionally any output of keypresses to Matlabs or Octaves
windows is suppressed. Use this with care, if your script aborts with an
error, Matlab or Octave may be left with a dead keyboard until the user
presses CTRL+C to reenable keyboard input. 'listenFlag' 2 is silently
ignored on Matlab in -nojvm mode under MS-Windows.

This function isn't entirely necessary to turn on listening as calling
GetChar, CharAvail, or FlushEvents will trigger listening on. However,
it is the only method by which to disable listening or switch between
suppression of keyboard input to Matlab and unsuppressed mode.

Please note that the commands ListenChar, CharAvail and GetChar are
subject to various constraints and limitations, depending on the
operating system you use, if you use Matlab in Java or -nojvm mode, if
you use Octave, if you have [Screen](/docs/Screen)\(\) onscreen windows open or not, or if
you use KbQueueXXX functions in parallel or not. Therefore use of these
functions can be troublesome for any but the most simple usages. Use of
KbCheck, KbWait, KbStroke/Press/ReleaseWait is often simpler if you are
just after keyboard input. Use of KbQueue functions, e.g., KbQueueCheck,
KbQueueWait, KbTriggerWait is better suited for background keystroke
collection. Use of KbEventAvail and KbEventGet is often more convenient,
more flexible and subject to less restrictions and gotchas than use of
GetChar et al.

# Some of the restrictions and caveats:

1. Works very well with Matlab and its Java based GUI enabled on Linux
and MacOSX, as well as on WindowsXP.

2. When used on Windows Vista or later \(Vista, Windows-7, Windows-8, ...\)
with Matlab's Java GUI, you cannot use any KbQueue functions at the same
time, ie., KbQueueCreate/Start/Stop/Check/Wait as well as KbWaitTrigger,
KbEventFlush, KbEventAvail, and KbEventGet are off limits after any call
to ListenChar, ListenChar\(1\), ListenChar\(2\), FlushEvents, CharAvail or
GetChar. You would need to call ListenChar\(0\) before you could call
KbQueueCreate and then use those functions. Vice versa, after a call to
KbQueueCreate, CharAvail, FlushEvents, and GetChar are dysfunctional and
ListenChar may be limited. You need to call KbQueueRelease before you can
use them again. This is generally true on MacOSX, and true for use of the
default keyboard \(the keyboard that GetChar et al. use\) on MS-Windows and
Linux. Use of other keyboards than the default keyboard, or of other
devices, e.g., mouse or joystick, is not prohibited during use of GetChar
et al.

3. If you use Matlab in "matlab -nojvm" mode without its GUI, or if you
use GNU/Octave instead of Matlab, the same restrictions as in 2. apply -
no parallel use of the default keyboards KbQueue - or any KbQueue on OSX
with GetChar et al. The only feature that works in parallel with KbQueues
is the suppression of spilling of keystroke characters into the Matlab or
Octave window during ListenChar\(2\) - at least on Linux and OSX, on
Windows this can't be prevented at all in "matlab -nojvm" mode. However,
if you switch to ListenChar\(2\) mode, you cannot break out of it by
pressing CTRL+C on Linux if the keyboard queue that is in parallel use
didn't get KbQueueStart called, ie. if it is stopped. On OSX with a
stopped Keyboard queue, neither CTRL+C nor stopping a runaway script
works.

4. On Linux, as a exception, some GetChar, CharAvail functionality may
still work in case 3. under certain conditions, e.g., if you don't use
ListenChar\(2\) and your Matlab/Octave is not in interactive mode.

Also, GetChar can only collect keystrokes from multiple connected
keyboards in case 1. In all other cases, it can only collect keystrokes,
or respond to press of CTRL+C, for the default keyboard device. It will
ignore other connected keyboards.

Basically: Mixing GetChar et al. and modern KbQueue functions is usually
not advisable, or if needed, great care must be taken to sidestep all the
mentioned limitations. Also the KbQueue functions usually have better
timing precision and allow to flexibly address multiple keyboards
separately at least on Linux.


For further explanation see help for "GetChar".
----

See also: GetChar


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/ListenChar.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/ListenChar.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/ListenChar.m</code>
</div>
