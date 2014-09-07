---
layout: mfile
title: GroupStructArrayByFields
categories:
  - PsychOneliners
encoding: UTF-8
---

theGroupedArray = GroupStructArrayByFields(theStructArray,theFields)

Group together the members of a struct array that share the same values
in the passed fields.

This is useful for sorting/grouping elements in a struct array on
parameters that signify membership of trials to a particular condition.

7/21/03  dhb  Wrote it.