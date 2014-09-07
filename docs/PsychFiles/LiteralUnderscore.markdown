---
layout: mfile
title: LiteralUnderscore
categories:
  - PsychFiles
encoding: UTF-8
---

str =  LiteralUnderscore(instr)

Some Matlab printing and plotting routines treat an
underscore as an instruction to subscript the next
character.  Calling this routine inserts a "\\" before
any "\_" in the passed string, so that it will come
out as passed.

SEE ALSO texlabel