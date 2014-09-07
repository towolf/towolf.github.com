---
layout: mfile
title: RemoveMatchingPaths
categories:
  - PsychOneliners
encoding: UTF-8
---

newPathList = RemoveMatchingPaths(pathList, matchString)

Removes any paths that contain the given matchString from the pathList.
If no pathList is specified, then the program sets pathList to the result
of the 'path' command.  This function returns a 'pathsep' delimited list
of paths, omitting the paths that contained the given matchString.