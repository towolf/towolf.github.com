---
layout: mfile
title: FileFromFolder
categories:
  - PsychFiles
encoding: UTF-8
---

[file,nfile] = FileFromFolder(folder,mode,ext)

Returns struct with all files in directory FOLDER.
MODE specifies whether an error is displayed when no directories are
found (default). If MODE is 'silent', only a message will will be
displayed in the command window, if 'ssilent', no notification will be
produced at all. If left empty, default is implied.
Ext is an optional filter on file extension. If specified, only files
with the specified extension will be found. It can be a cell vector of
strings for filtering on multiple extensions