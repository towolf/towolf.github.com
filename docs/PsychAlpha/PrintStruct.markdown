---
layout: mfile
title: PrintStruct
categories:
  - PsychAlpha
encoding: UTF-8
---

function PrintStruct(dataStruct, [filePtr], [indentChar], [numIndentSpaces], [numberFormat])

Display the contents of struct arrays to arbitrary nesting depth.  By
default PrintStruct prints to the MATLAB command window. If a file
pointer argument is supplied then it prints the contents of the struct
to a file.

Nested fields within the struct are indented numIndentSpaces for each level
of nesting.  numIndenSpace is equal to one space.  The indentation character
by default is the space character.

Pass the empty vector, "[ ]" for either optional argument to specify
the default.

PrintStruct was suggested by Marialuisa Martelli as a convenient way to
display experiment parameters and results stored in struct. It's still
experimental.  The readability of the output could be improved by
including array indices in the output along with the struct field  names.
Communicating that by using indentiation and spacing does not work well
for complicated structures and large arrays.
