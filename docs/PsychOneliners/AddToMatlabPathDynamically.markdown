---
layout: mfile
title: AddToMatlabPathDynamically
categories:
  - PsychOneliners
encoding: UTF-8
---

AddToMatlabPathDynamically(directory)

Add the directory and its subdirectories to Matlab's path, dynamically,
with strippint out of .svn and .git directories.

Use for for putting routines onto path that are specifict to a particular
project, without them staying around and clogging up the name space.

Typical usages:
a) When getting version info
  exp.mFileName = mfilename;
  [exp.versionInfo,exp.codeDir] = GetAllVersionInfo(exp.mFileName);
  AddToMatlabPathDynamically(exp.codeDir);

b) Direct call
  AddToMatlabPathDynamically( fileparts(which(mfilename)));

7/12/13  dhb  Wrote it.
7/25/14  dhb  Make independent of BrainardLab idiosyncracies.