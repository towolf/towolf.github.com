---
layout: mfile
title: RemoveSVNPaths
categories:
  - PsychOneliners
encoding: UTF-8
---

newPathList = RemoveSVNPaths\(pathList\)
Removes any .svn paths from the pathList.  If no pathList is specified,
then the program sets pathList to the result of the 'path' command.  This
function returns a 'pathsep' delimited list of paths omitting the .svn
paths.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/RemoveSVNPaths.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/RemoveSVNPaths.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/RemoveSVNPaths.m</code>
</div>
