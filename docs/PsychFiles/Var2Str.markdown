---
layout: mfile
title: Var2Str
categories:
  - PsychFiles
encoding: UTF-8
---

str = Var2Str(in,name)

Takes variable IN and creates a string representation of it that would
return the original variable when fed to eval(). NAME is the name of the variable
that will be printed in this string.
Can process any (combination of) MATLAB built-in datatype

examples:
  Var2Str({4,7,'test',@exp})
  ans =
      {4,7,'test',@exp}

  var.field1.field2 = {logical(1),'yar',int32(43),[3 6 1 2],@isempty};
  Var2Str(var,'var2')
  ans =
      var2.field1.field2 = {true,'yar',int32(43),[3,6,1,2],@isempty};