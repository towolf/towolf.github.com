---
layout: mfile
title: SetSourceAlpha
categories:
  - PsychAlphaBlending
encoding: UTF-8
---

[newSourceMat, newDestinationMat]=SetSourceAlpha(SourceFactorStr, alpha, sourceImage, destinationImage)

Given an alpha blending factor, "sourceFactorStr", insert "alpha"
into the source or destination image such that on alpha blending with the
specified sourceFactorStr "alpha" is selected as the destination
alpha.

For some combinations of destination factor string and source factor
string, SetSourceAlpha may undo a subsequent call to SetDestinationAlpha
or be undone by a previous call to SetDestinationAlpha.  This happens
when both the destination factor string and the source factor string
specify the same location of alpha values yet store different alpha
values.  For example, if both the source alpha and destination alpha are
drawn from the source alpha plane (GL\_SRC\_ALPHA)  then setting the source
alpha to 0 would also change the destination alpha to 0.  Both source and
destination surfaces would share the source surface alpha plane for
storage of the alpha value.

SetAlphaDestination helps test OpenGL alpha blending precision.

see also: PsychAlphaBlending