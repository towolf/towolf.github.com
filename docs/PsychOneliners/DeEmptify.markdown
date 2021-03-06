---
layout: mfile
title: DeEmptify
categories:
  - PsychOneliners
encoding: UTF-8
---

in = DeEmptify(in,column)
deletes empty cells or rows from cellarray:

- if only IN is specified, IN has to be a vector. IN will be returned
  with all empty cells deleted
- if IN is a matrix, COLUMN must be specified. Rows are only
  deleted from IN when an empty cell is encountered in a column
  specified in COLUMN. COLUMN can be a vector

Example:
  DeEmptify({'','r','','re'})
  ans =
      'r'    're'

  a = {'p' 'r'  ''; ...
       '' 're' 'r'}

  DeEmptify(a,3)
  ans =
       ''    're'    'r'

  DeEmptify(a,1)
  ans =
       'p'   'r'     ''

  DeEmptify(a,1) or DeEmptify(a,[1 3])
  ans =
      Empty cell array: 0-by-3