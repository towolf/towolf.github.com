---
layout: mfile
title: FindFolder
categories:
  - PsychFiles
encoding: UTF-8
---

directory=FindFolder(name)
Searches the Matlab 'path' for the path to the named folder.
There may be no matches, one match, or multiple matches.
Each unique match appears as a row in "directory".
If there are no matches then "directory" will be an empty matrix.
Matching ignores case.
You should DEBLANK a row of "directory" before using it.

Also see Matlab's MKDIR, TEMPDIR, ISDIR, LOOKFOR, WHAT.
Try HELP PsychFiles.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychFiles/FindFolder.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychFiles/FindFolder.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychFiles/FindFolder.m</code>
</div>
