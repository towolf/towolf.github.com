---
layout: mfile
title: GetSubversionPath
categories:
  - PsychOneliners
encoding: UTF-8
---

svnpath = GetSubversionPath -- Return auto-detected installation path
for svn client, if any. Return empty string if auto-detection not
possible. Typical usage is like this:

mysvncommand = [GetSubversionPath 'svn status']; system(mysvncommand);

GetSubversionPath will return the path to be prefixed in front of the svn
executable. If none can be found, the svn executable will be executed
without path spec. If it is installed in the system executable search
path, it will then still work.

The function simply checks if the svn executable is in the Matlab path
and returns a proper path-spec. If it isn't found in the Matlab path, it
tries default path locations for OS-X and Windows. If that doesn't work,
it returns an empty string.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetSubversionPath.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetSubversionPath.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetSubversionPath.m</code>
</div>
