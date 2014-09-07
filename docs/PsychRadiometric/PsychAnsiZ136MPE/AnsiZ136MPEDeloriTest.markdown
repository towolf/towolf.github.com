---
layout: mfile
title: AnsiZ136MPEDeloriTest
categories:
  - PsychAnsiZ136MPE
encoding: UTF-8
---

AnsiZ136DeloriTest

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the AnsiZ136 routines, please see the notes on usage
and responsibility in PsychAnsiZ136MPE/Contents.m (type "help PsychAnsiZ136MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Tests radiometric calculations and light safety calculations.

Reads in tab delimted text file AnsiZ136MPEDeloriTestInput.txt that has a set of
rows in it.  Each row provides stimulus properties for a monochromtic
light and values obtained from Delori's spreadsheet.
(There are also some other test values entered by hand in the text file, for
other radiometric quanties that I could not find computed in Delori's spreadsheet.)

Delori's spreadsheet is described in footnote 49 of Delori et al. (2007,
JOSA A, 24, pp.1250-1265).  That footnote indicates that the spreadsheet
will be shared as long as recipients accept full responsibility for its use.
The version of Delori's spreadsheet used to get these numbers is 0cLC\_0.9.9.