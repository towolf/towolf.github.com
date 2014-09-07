---
layout: mfile
title: PsychOpenEyes
categories:
  - PsychVideoCapture
encoding: UTF-8
---

result = PsychOpenEyes(cmd, handle [, arg1, arg2, ...]);

PsychOpenEyes controls Psychtoolboxs built-in computer vision based eye
tracker, based on the free-software open-source "OpenEyes" toolkit.

Syntax: result = PsychOpenEyes(command, handle, optional arguments...);

'command' is a subcommand, similar to the subcommands in [Screen](/docs/Screen)() and
other PTB functions.

'handle' A numeric handle to the tracker connection. Currently you should
just pass zero (0) as handle.

'arg1, arg2, ...' Optional arguments for different subcommands.


# Subcommand and their syntax/meaning:

PsychOpenEyes('OpenTracker')