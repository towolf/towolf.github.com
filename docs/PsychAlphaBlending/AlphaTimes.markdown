---
layout: mfile
title: AlphaTimes
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

matProduct=AlphaTimes(mat1, alpha)

Calculate the product of an image matrix and alpha as would [Screen](/docs/Screen) Alpha
blending: Pointwise multiply and round.  Argument 'alpha' may
be either a scaler or the alpha plane.   If an alpha plane, it must have
the same x y dimensions of argument 'mat'.

see also: AlphaSum, PsychAlphaBlending