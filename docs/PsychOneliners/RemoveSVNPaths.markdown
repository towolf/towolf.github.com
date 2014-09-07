---
layout: mfile
title: RemoveSVNPaths
categories:
  - PsychOneliners
encoding: UTF-8
---

newPathList = RemoveSVNPaths(pathList)
Removes any .svn paths from the pathList.  If no pathList is specified,
then the program sets pathList to the result of the 'path' command.  This
function returns a 'pathsep' delimited list of paths omitting the .svn
paths.