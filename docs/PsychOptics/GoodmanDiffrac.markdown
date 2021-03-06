---
layout: mfile
title: GoodmanDiffrac
categories:
  - PsychOptics
encoding: UTF-8
---

mtf = GoodmanDiffrac(s,s0)

Compute Equation 6-31 from page 120 of Goodman.
This is the diffraction-limited optical MTF,
computed given the coherent diffraction limit s0.

Goodman, J. W. (1968) Introduction to Fourier Optics.
San Francisco: McGraw-Hill.

Note that in the Williams et al. paper (ref??), this
formula is given for the incoherent diffraction limit,
which is twice the coherent limit.

Also see DiffractionMTF.