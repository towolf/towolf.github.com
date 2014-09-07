---
layout: mfile
title: ShiftSpectra
categories:
  - PsychColorimetric
encoding: UTF-8
---

out = ShiftSpectra(in,Sin,shift)

Shift spectra along wavelength axis.  Works
on a single row vector.  Should probably
be generalized to handle a whole set
of color matching functions.

11/23/98  dhb  Wrote it.
8/16/00   dhb  Modify to handle row or column vector input.