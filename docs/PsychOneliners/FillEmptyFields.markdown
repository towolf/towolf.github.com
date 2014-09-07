---
layout: mfile
title: FillEmptyFields
categories:
  - PsychOneliners
encoding: UTF-8
---

in = FillEmptyFields(in,filling)

If input is a struct (-array):
Fills all empty fields in IN with FILLING
Also operates on N-D struct arrays

If input is a cell (-array):
Fills all empty elements in IN with FILLING

DN    2008
DN    2008-05-29 Shortened it
DN    2008-05-31 added cell support
DN    2012-06-12 fixed bug where only first element in struct array was
                 operated on