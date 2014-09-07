---
layout: mfile
title: GetSVNInfo
categories:
  - PsychOneliners
encoding: UTF-8
---

 svnInfo = GetSVNInfo(directoryOrFile)

 Description:
 Retrieves the svn information on a specified directory or file.  This is
 essentially a wrapper around the shell command "svn info".

 Input:
 directoryOrFile (string) - Directory or file name of interest.

 Output:
 svnInfo (struct) - Structure containing the following information:
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