---
layout: mfile
title: GetCharTest
categories:
  - PsychTests
encoding: UTF-8
---

GetCharTest([startAt])

Test the Psychtoolbox function "GetChar".

For platforms such as OS X where GetCharTest is divided into subtests,
begin at subtest "startAt" if it is in the allowable range.  Otherwise
ignore the argument and begin with the first subtest.

GetCharTest tests GetChar for likely failure modes. It also tests associated
functions for character events, such as CharAvail, ListenChar and FlushEvents.