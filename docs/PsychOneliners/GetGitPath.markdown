---
layout: mfile
title: GetGitPath
categories:
  - PsychOneliners
encoding: UTF-8
---

gitpath = GetGitPath -- Return auto-detected installation path
for git client, if any. Return empty string if auto-detection not
possible. Typical usage is like this:

mygitcommand = [GetGitPath 'git describe']; system(mygitcommand);

GetGitPath will return the path to be prefixed in front of the git
executable. If none can be found, the git executable will be executed
without path spec. If it is installed in the system executable search
path, it will then still work.

The function simply checks if the git executable is in the Matlab path
and returns a proper path-spec. If it isn't found in the Matlab path, it
tries default path locations for OS-X and Windows. If that doesn't work,
it returns an empty string.