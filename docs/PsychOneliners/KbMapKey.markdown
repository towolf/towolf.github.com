---
layout: mfile
title: KbMapKey
categories:
  - PsychOneliners
encoding: UTF-8
---

q = KbMapKey(KeyNums,keyCode)
Checks if any of specified keys is depressed
input: vector of key numbers, keystate boolean vector as returned by e.g.
       KbCheck.
output: boolean vector specifying true for every key when its depressed

SEE ALSO: KbCheck