---
layout: mfile
title: KbName
categories:
  - PsychBasic
encoding: UTF-8
---

kbNameResult = KbName\(arg\)

    KbName maps between KbCheck-style keyscan codes and key names.

    \* If arg is a string designating a key label then KbName returns the
      keycode of the indicated key.

    \* If arg is a keycode, KbName returns the label of the designated key.

    \* If no argument is supplied then KbName waits one second and then
    calls KbCheck.  KbName then returns a cell array holding the names of
    all keys which were down at the time of the KbCheck call. The
    one-second delay preceeding the call to KbCheck avoids catching the
    <return\> keypress used to execute the KbName function.

  \* If arg is 'UnifyKeyNames', KbName will switch its internal naming
    scheme from the operating system specific scheme \(which was used in
    the old Psychtoolboxes on MacOS-9 and on Windows\) to the MacOS-X
    naming scheme, thereby allowing to use one common naming scheme for
    all operating systems, increasing portability of scripts. It is
    recommended to call KbName\('UnifyKeyNames'\); at the beginning of each
    new experiment script.
      CAUTION: This function may contain bugs. Please report them \(or fix
      them\) if you find some.

  \* If arg is 'KeyNames', KbName will print out a table of all
    keycodes-\>keynames mappings.

  \* If arg is 'KeyNamesOSX', KbName will print out a table of all
    keycodes-\>keynames mappings for MacOS-X.

  \* If arg is 'KeyNamesOS9', KbName will print out a table of all
    keycodes-\>keynames mappings for MacOS-9.

  \* If arg is 'KeyNamesWindows', KbName will print out a table of all
    keycodes-\>keynames mappings for M$-Windows.

  \* If arg is 'KeyNamesLinux', KbName will print out a table of all
    keycodes-\>keynames mappings for GNU/Linux, X11.

    KbName deals with keys, not characters. See KbCheck help for an
    explanation of keys, characters, and keycodes.

  Please note that KbName always assumes a US keyboard layout. Changing
  the keyboard layout settings in your operating system will have no
  effect. If a keyboard with non-US layout is connected, e.g, a german
  keyboard layout, then certain keys may not match. E.g., on a german
  keyboard, the 'Y' key will be reported as 'Z' key and the 'Z' key will
  be reported as 'Y' key, because these two keys are interchanged on the
  german keyboard wrt. the US keyboard.

    There are standard character sets, but there are no standard key
    names.  The convention KbName follows is to name keys with  the primary
    key label printed on the key.  For example, the the "\]\}"  key is named
    "\]" because "\]" is the primary key label and "\}" is the  shifted key
    function.  In the case of  labels such as "5", which appears  on two
    keys, the name "5" designates the "5" key on the numeric keypad  and
    "5%" designates the QWERTY "5" key. Here, "5" specifies the primary
    label of the key and the shifted label, "%" refines the specification,
    distinguishing it from keypad "5".  Keys labeled with symbols not
    represented in character sets are assigned names describing those
    symbols  or the key function, for example the space bar is named
    "space" and the apple  key is named "apple".  Some keyboards have
    identically-labelled keys distinguished
  only by their positions on the keyboard, for example, left and right
  shift  keys.  Windows operating systems more recent than Windows 95 can
  distinguish between such keys.  To name such keys, we precede the key
  label with either  "left\_" or "right\_", to create the key name.  For
  example, the left shift key  is called "left\_shift".

    Use KbName to make your scripts more readable and portable, using key
    labels instead of keycodes, which are cryptic and vary between Mac and
    Windows computers.

    For example,

    yesKey = KbName\('return'\);
    \[a,b,keyCode\] = KbCheck;
    if keyCode\(yesKey\)
        flushevents\('keyDown'\);
        ...
    end;

OS X \_ OS9 \_ Windows \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

  OS X, OS 9 and Windows versions of KbCheck return different keycodes.
  You can mostly  overcome those differences by using KbName, but with
  some complications:

  While most keynames are shared between Windows and Macintosh, not all
  are. Some key names are used only on Windows, and other key names are
  used only on Macintosh. For a lists of key names common to both
  platforms and unique to each see the comments in the  body of KbName.m.

  KbName will try to use a mostly shared name mapping if you add the
  command KbName\('UnifyKeyNames'\); at the top of your experiment script.
  At least the names of special keys like cursor keys, function keys and
  such will be shared between the operating systems then.

  Your computer might be able to distinguish between identically named
  keys.  For example, left and right shift keys, or the "enter" key on
  the keyboard and the enter key on the numeric keypad. Which of these
  keys it can destinguish depends on the operating system. For details,
  see comments in the body of KbName.m.

  Historically, different operating systems used different keycodes
  because they used different types of keyboards: PS/2 for Windows, ADB
  for OS 9, and USB for OS 9, Windows, and OSX.  KbCheck on OS X returns
  USB keycodes.
----

    See also KbCheck, KbDemo, KbWait.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/KbName.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/KbName.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/KbName.m</code>
</div>
