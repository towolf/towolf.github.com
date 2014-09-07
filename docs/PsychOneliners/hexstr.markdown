---
layout: mfile
title: hexstr
categories:
  - PsychOneliners
encoding: UTF-8
---

str=[hexstr](/docs/hexstr)(n)
Convert any number to a hex string representing the lower 32 bits,
emulating the C format %lx for a long. This works with both positive and
negative numbers, unlike the MATLAB format %x (and %tx and %bx) which
can't deal with negative numbers.

fprintf('Error 0x%s.\\n',[hexstr](/docs/hexstr)(err));

See also DEC2HEX, FPRINTF.