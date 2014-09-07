---
layout: mfile
title: FolderFromFolder
categories:
  - PsychFiles
encoding: UTF-8
---

[fold,nfold] = FolderFromFolder(folder,mode)

Returns struct with all directories in directory FOLDER.
MODE specifies whether an error is displayed when no directories are
found (default). If MODE is 'silent', only a message will will be
displayed in the command window, if 'ssilent', no notification will be
produced at all.