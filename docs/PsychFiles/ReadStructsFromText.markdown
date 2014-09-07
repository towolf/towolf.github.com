---
layout: mfile
title: ReadStructsFromText
categories:
  - PsychFiles
encoding: UTF-8
---

theStructs = ReadStructsFromText(filename)

Open a tab delimited text file.  The first row should
contain the field names for a structure.  Each following
row contains the data for one instance of that structure.

This routine reads each row and returns an array of structures,
one struct for each row, with the data filled in.  Data
can be numeric or string for each field.

Not a lot of checking is done for cases where the read file
fails to conform to the necessary format.

See Also: WriteStructsToText