---
layout: mfile
title: PrimaryToGamut
categories:
  - PsychCal
encoding: UTF-8
---

 [gamut, badIndex] = PrimaryToGamut(cal,primary)

 Check that primary coordinates are in range [0,1].
 Force them to be so if not.  The indices of the
 out of gamut primary settings are returned as 'badIndex'.

 9/8/93    jms   Set global flag if there was a gamut problem.
 9/13/93   jms   Took out the global flag and instead return
                 a flag vector for the ones that were changed.
 9/26/93      dhb   Added calData argument.  It is not used, but
                 I want to pass it through these routines generally
 9/27/93   jms   Commented out the messages for going out of gamut.
    3/7/94      dhb     Modified so that badIndex return respects tolerance.
 4/5/02    dhb, ly  New naming convention.