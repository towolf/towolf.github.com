---
layout: mfile
title: AltSize
categories:
  - PsychOneliners
encoding: UTF-8
---

varargout = AltSize(in,arg)

extends size()'s functionality to support querying the size of multiple
dimensions of a variable in one call.
requested dimensions can be repeated and may (of course) be singleton
number of output arguments must match number of requested dimension sizes
or be one, in which case a vector is returned

example:
    in = ones(1,2,3,4,5);
    [d e f g h i] = AltSize(in,[1 3 2 8 4 2])
    d =
         1
    e =
         3
    f =
         2
    g =
         1
    h =
         4
    i =
         2