---
layout: mfile
title: MakeMonotonic
categories:
  - PsychGamma
encoding: UTF-8
---

output = MakeMonotonic(input)

Make input monotonically increasing.

See also MakeGammaMonotonic, which is probably what you want if you are fitting
gamma functions.  This routine left alone when MakeGammaMonotonic was created,
in case it is called from programs completely unrelated to gamma fitting.

3/1/99  dhb  Handle multiple columns.
8/03/07 dhb  Old routine just enforced non-decreasing.  Fixed to make strictly increasing.
3/07/10 dhb  Added comment about MakeGammaMonotonic.