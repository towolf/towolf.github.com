---
layout: mfile
title: GetSVNInfo
categories:
  - PsychOneliners
---

 svnInfo = GetSVNInfo\(directoryOrFile\)

 Description:
 Retrieves the svn information on a specified directory or file.  This is
 essentially a wrapper around the shell command "svn info".

 Input:
 directoryOrFile \(string\) \- Directory or file name of interest.

 Output:
 svnInfo \(struct\) \- Structure containing the following information:
   Path
    URL
    RepositoryRoot
    RepositoryUUID
    Revision
    NodeKind
    Schedule
    LastChangedAuthor
    LastChangedRev
    LastChangedDate

    'svnInfo' will be empty if there is no svn info for 'directoryOrFile'.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetSVNInfo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetSVNInfo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetSVNInfo.m</code>
</div>
