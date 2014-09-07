---
layout: mfile
title: AssignGetCharJava
categories:
  - PsychJava
encoding: UTF-8
---

AssignGetCharJava - Helper function for Java based GetChar.

This routine is called during initialization from ListenChar,
CharAvail, GetChar and FlushEvents. It tries as hard as possible
instantiate a Java object of the GetCharJava class and returns it
if successfull. Different versions of Matlab use different versions
of the Java virtual machine. Matlab can only load versions of
GetCharJava.class that were compiled with the same Java version as
the one that Matlab uses. Therefore we provide multiple versions of
the GetCharJava.class, each compiled against a different Java version.
We try to instantiate the newest version. If that fails, we try the
2nd newest version, and so on. If all versions bundled with PTB failed
to instantiate, the behaviour depends on the availability of an installed
Java compiler. If a "javac" compiler is available, as on MacOS-X, we invoke
it on the source code to built a customized version of GetCharJava for that
machine. Otherwise we give up and fail.