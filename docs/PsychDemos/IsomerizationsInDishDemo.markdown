---
layout: mfile
title: IsomerizationsInDishDemo
categories:
  - PsychDemos
encoding: UTF-8
---

IsomerizationsInDishDemo

Shows how to compute photoreceptor isomerizations using toolbox
routines.  These calculations are for a retinal preparation
that consists of a retina in a dish and thus do not include
any preretinal absorption.  Parameters are set up for a
Guinea Pig retina.  The file spd\_apparatusrel.mat contains
the relative spectrum of the light with respect to which
the computation is accomplished.

NOTE, DHB, 7/19/13. This demo routine and its associated data routines
(DefaultPhotoreceptors, FillInPhotoreceptors, PrintPhotoreceptors)
should be better integrated with the more recent code that
implements the CIE physiological cone fundamentals, and the
whole set of stuff should be better documented.  See also
   IsomerizationsInDishDemo
   CIEConeFundamentalsTest
   ComputeCIEConeFundamentals
   ComputeRawConeFundamentals
   DefaultPhotoreceptors
   FillInPhotoreceptors
   PrintPhotoreceptors
   RetIrradianceToIsoRecSec
In particular, there should be some default for the
photoreceptors structure that gives one the CIE cone
fundamentals in all their parametric glory, plus additional
parameters that yield real energy/quantal sensitivites so
that the resulting coordinates are isomerization rates in
real units.  I think that we're close to having that, but
better documentation and tidying is needed.

05/06/03 lyin Wrote it.
06/26/03 dhb    Rewrote to be self-contained, plus new calling conventions.
07/10/03 dhb  Various tuning.
07/11/03 dhb  Grab data through subroutines.  Get rid of integration time.
04/2/13  dhb  Change clear all to clear, and close figs.
04/27/13 dhb  Improve comments.
7/19/13  dhb  Print out photoreceptors structure using PrintPhotoreceptors.
8/11/13  dhb  Protect against case when absorbance is provided directly.
05/26/14 dhb  Dusted off.