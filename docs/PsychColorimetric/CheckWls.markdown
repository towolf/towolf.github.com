---
layout: mfile
title: CheckWls
categories:
  - PsychColorimetric
encoding: UTF-8
---

[errorRet] = CheckWls(wls1,wls2,[quiet])

Check that two wavelength descriptions are consistent with
the same underlying sampling.

Arguments may be either[start delta n],
a list of wavelengths, or a struct.

errorRet indicates status
  \== 0: OK
  \== 1: Mismatch

Arg quiet tells function whether or not to print display to
screen notifying user that check failed:
    0 =\> display message
  else =\> keep quiet

9/13/93  dhb  Added error return, no longer exits on error.
3/12/99  xmz  Took care of cases when wls1 and wls2 are not
              equal in length.
1/4/00   mpr  Added quiet flag to suppress display.
4/22/04  dhb  Make quiet the default.