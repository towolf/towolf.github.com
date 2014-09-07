---
layout: mfile
title: GetChar
categories:
  - PsychBasic
encoding: UTF-8
---

[ch, when] = GetChar([getExtendedData], [getRawCode])

Wait for a typed character and return it.  If a character was typed
before calling GetChar then GetChar will return that character immediatly.
Characters flushed by FlushEvents are all ignored by GetChar. Characters
are returned in the first return argument "ch".

Please read the 'help ListenChar' carefully to understand various
limitations and caveats of this function, and to learn about - often
better - alternatives.

CAUTION: Do not rely on the keypress timestamps returned by GetChar
without fully reading and understanding this help text. Run your own
timing tests on GetChar and KbCheck to verify that the timing is good
enough and avoid GetChar for timed keypresses if possible at all. Use
KbWait and KbCheck instead.

The main purpose of GetChar is to reliably collect keyboard input in the
background while your experiment script is occupied with performing other
operations, e.g., Matlab computations, sound output or visual stimulus
drawing. After an initial call to ListenChar, the operating system will
record all keyboard input into an internal queue. GetChar removes
characters from that queue, one character per invocation of GetChar. You
can empty that queue any time by calling FlushEvents('keyDown').

If you want to check the current state of the keyboard, e.g., for
triggering immediate actions in response to a key press, waiting for a
subjects response, synchronizing to keytriggers (e.g., fMRI machines) or
if you require high timing precision then use KbCheck instead of GetChar.

GetChar should work on all platforms, but its specific functionality,
beyond simply returning typed characters, will vary depending on OS type
and version, if you use Matlab or Octave, and if you use Matlab with or
without Java based GUI active. For portability it is therefore best to
ignore all info returned beyond the character code.

"when" is a struct. It (used to) return the time of the keypress, the "adb"
address of the input device, and the state of all the modifier keys
(shift, control, command, option, alphaLock) and the mouse button.
"when.secs" is an estimate, of what GetSecs would have been. Since it's
derived sometime from a timebase different from the timebase of GetSecs,
times returned by GetSecs are not directly comparable to when.secs.

By setting getExtendedData to 0, all extended timing/modifier information
will not be collected and "when" will be returned empty.  This speeds up
calls to this function. If ommitted or set to 1, the "when" data
structure is filled.  getRawCode set to 1 will set "ch" to be the integer
ACII code of the available character.  If ommitted or set to 0, "ch" will
be in char format. When running under Linux in "matlab -nojvm" mode or on
Octave, "when" will be returned empty. When running on any other
operating system under Octave or in "matlab -nojvm" mode, or on Windows
Vista and later versions of the Windows OS, when will only contain a
valid timestamp, but all other fields will be meaningless.

GetChar and CharAvail are character-oriented (and slow), whereas KbCheck
and KbWait are keypress-oriented (and fast). If only a meta key (like
\<option\> or \<shift\>) was hit, KbCheck will return true, because a key was
pressed, but CharAvail will return false, because no character was
generated. See KbCheck.

CharAvail and GetChar use the system event queue to retrieve the character
generated, not the raw key press(es) per se. If the user presses "a",
GetChar returns 'a', but if the user presses option-e followed by "a",
this selects an accented a, "?", which is treated by GetChar as a single
character, even though it took the user three keypresses (counting the
option key) to produce it.

There can be some delay between when the key is pressed and when CharAvail
or GetChar detects it, due to internal processing overhead in Matlabs Java
implementation. GetChar internally collects timestamps in the timebase
used by Matlabs Java implementation, whereas other Psychtoolbox timing functions
(GetSecs, [Screen](/docs/Screen)('[Flip](/docs/Flip)'), KbCheck, KbWait, ...) use time reported by some
high precision system timer. The "when.secs" time reported by GetChar is
converted from Java timebase to Psychtoolboxs timebase. Due to conversion
errors mostly out of our control, the reported values can be off by
multiple dozen or even hundreds of milliseconds from what KbWait, KbCheck
or GetSecs would report. Example: A high-end Pentium-4 3.2 Ghz system
running Windows-XP has been measured to be off by 40 to 70 milliseconds.

Some Java implementations are also known to have problems/bugs in
timestamping keyboard presses properly and each Matlab version on each
operating system is bundled with a different Java version, so some Matlab
versions may be reliable with respect to GetChars timing, whereas others
are not.

---\> If precise timing of the keypress is important, use KbCheck or
KbWait or KbQueueXXX functions or KbEventGet for consistent results!

# OS X / Windows-XP / Linux with Matlab and Java enabled

JAVA PATH: The GetChar implementation for Matlab is based on Java.
Therefore, the Psychtoolbox subfolder PsychJava must be added to Matlabs
static classpath. Normally this is done by the Psychtoolbox installer by
editing the Matlab file "classpath.txt" (enter which('classpath.txt') to
find the location of that file). If the installer fails to edit the file
properly, you'll need to perform that step manually by following the
instructions of the installer. See 'help PsychJavaTrouble' for more infos
on this.

KEYSTROKES IN THE BACKGROUND: To detect keypresses made before the
GetChar call, you must have called "ListenChar" earlier.  ListenChar
redirects keystrokes to the GetChar queue. Calling ListenChar at the
beginning of your script should cause GetChar to behave identically
to OS 9 GetChar with respect to background keystroke collection.

KEYSTROKES IN MATLAB WINDOW: By default, all keystrokes are also sent to
Matlabs window, generating some ugly clutter. You can suppress this by
calling ListenChar(2), so your Matlab console stays nice and clean. Don't
forget to call ListenChar(1) or ListenChar(0) though before the end of
your script. If Matlab returns to its command prompt without reenabling
keyboard input via ListenChar(0) or ListenChar(1), Matlab will be left
with a dead keyboard until you press the CTRL+C key combo. This silencing
of clutter does currently not work in matlab -nojvm mode, or if you use
GNU/Octave instead of Matlab.

OTHER "when" RETURN ARGUMENT FIELDS: Owing to differences in what
accessory information the underlying operating systems provides about
keystrokes, "when' return argument fields differs between operating systems.
GetChar sets fields for which it returns no value to the value 'Nan'.

See also: ListenChar, CharAvail, FlushEvents, TestGetChar, KbCheck,
KbWait


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/GetChar.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/GetChar.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/GetChar.m</code>
</div>
