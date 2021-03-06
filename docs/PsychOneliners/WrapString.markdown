---
layout: mfile
title: WrapString
categories:
  - PsychOneliners
encoding: UTF-8
---

wrappedString=WrapString(string,[maxLineLength])

Wraps text by changing spaces into linebreaks '\\n', making each line as
long as possible without exceeding maxLineLength (default 74
characters). WrapString does not break words, even if you have a word
that exceeds maxLineLength. The returned "wrappedString" is identical to
the supplied "string" except for the conversion of some spaces into
linebreaks. Besides making the text look pretty, wrapping the text will
make the printout narrow enough that it can be sent by email and
received as sent, not made hard to read by mindless breaking of every
line.

Note that this schemes is based on counting characters, not pixels, so
it will give a fairly even right margin only for monospaced fonts, not
proportionally spaced fonts. The more general solution would be based on
counting pixels, not characters, using either [Screen](/docs/Screen) 'TextWidth' or
TextBounds.