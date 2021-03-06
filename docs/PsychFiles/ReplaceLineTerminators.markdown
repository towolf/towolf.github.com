---
layout: mfile
title: ReplaceLineTerminators
categories:
  - PsychFiles
encoding: UTF-8
---

newStr=ReplaceLineTerminators(str, newTerminator)

[Replace](/docs/Replace) either mac, windows, or linux style line terminators in the
string "str" with the the specified line terminator and return the
result. Strings containing Macintosh, Windows or Unix line terminators
(see below), or any mix thereof are handled as input.

The argument "newTerminator" may be either the terminator characters
which you want to substitute in or else a string identifying a
platform. If you provide terminators, these must be a combination of [
\\f\\n\\r\\t\\v], while terminators for the desired platform can be specified
by the identifiers in teh middle column below:

      Macintosh:      'Mac', 'Macintosh', 'OS 9' 'OS9'        CR      13
      Windows:        'Win', 'Windows', 'DOS', 'MSDOS'        CRLF    13 10
      Unix:           'Unix','Linux', 'BSD', 'OS X', 'OSX'    LF      10

SEE ALSO: BreakLines