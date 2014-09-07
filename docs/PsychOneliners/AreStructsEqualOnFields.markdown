---
layout: mfile
title: AreStructsEqualOnFields
categories:
  - PsychOneliners
encoding: UTF-8
---

areEqual = AreStructsEqualOnFields(struct1,struct2,theFields)

Returns 1 if two structs share the same value on each of the passed
fields, 0 otherwise.  The equality of each field in the two structs is
checked with a call to isequal()

5/1/05     dhb, jmk   Handle cell and struct fields, a little bit.
2012/06/12 DN         Can now handle fields of any data type supported by
                      isequal(). Added some input checks