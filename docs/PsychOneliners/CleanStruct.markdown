---
layout: mfile
title: CleanStruct
categories:
  - PsychOneliners
encoding: UTF-8
---

out = CleanStruct(temp,qrec)

Deletes all empty structs from a struct array
Deletes all empty fields from a struct (array)

if QREC == true (default is false), recurses through the struct and also
cleans any nested structs it encounters in the struct

DN    2007