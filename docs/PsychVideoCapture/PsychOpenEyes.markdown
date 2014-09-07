---
layout: mfile
title: PsychOpenEyes
categories:
  - PsychVideoCapture
---

result = PsychOpenEyes\(cmd, handle \[, arg1, arg2, ...\]\);

PsychOpenEyes controls Psychtoolboxs built\-in computer vision based eye
tracker, based on the free\-software open\-source "OpenEyes" toolkit.

Syntax: result = PsychOpenEyes\(command, handle, optional arguments...\);

'command' is a subcommand, similar to the subcommands in [Screen](/docs/Screen)\(\) and
other PTB functions.

'handle' A numeric handle to the tracker connection. Currently you should
just pass zero \(0\) as handle.

'arg1, arg2, ...' Optional arguments for different subcommands.


# Subcommand and their syntax/meaning:

PsychOpenEyes\('OpenTracker'\)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychVideoCapture/PsychOpenEyes.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychVideoCapture/PsychOpenEyes.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychVideoCapture/PsychOpenEyes.m</code>
</div>
