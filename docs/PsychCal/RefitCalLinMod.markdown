---
layout: mfile
title: RefitCalLinMod
categories:
  - PsychCal
encoding: UTF-8
---

RefitCalLinMod

Refit the calibration linear model.

3/27/02  dhb            Wrote it.
9/26/08  dhb, ijk, tyl  Simplify naming possibilities.
9/27/08  dhb            Clearer defaults for prompts.  Pass number of levels to dacsize routine.
2/15/10  dhb            Plot all components of gamma functions.
5/28/10  dhb            Add yoked fitting routine to calls.  Should have no effect when yoked isn't set, but
                        do the right thing when it is.
6/5/10   dhb            Make it work when rawGammaInput has multiple columns.  Use plot subroutines.