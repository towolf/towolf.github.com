---
layout: mfile
title: FindEpsWeibTAFC
categories:
  - Psychometric
encoding: UTF-8
---

epsilon = FindEpsWeibTAFC(pCorrect,beta)

Compute the epsilon corresponding to a particular
percent correct.  Mainly used with quest.

Note that this is a less flexible version of the
computation performed by QUEST('Epsilon').  This
routine does not allow variations in gamma, delta
or the psychometric function.  It agrees with
what QUEST('Epsilon') computes for gamma = 0.5,
delta = 0, Weibull function.

It would not be hard to fix this to include delta
and gamma as parameters, but QUEST('Epsilon') seems
to do the trick.

8/26/94     ccc, dhb        Wrote it.
8/30/94     dhb                 Comment comparing to QUEST('Epsilon').