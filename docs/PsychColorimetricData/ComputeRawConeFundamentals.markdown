---
layout: mfile
title: ComputeRawConeFundamentals
categories:
  - PsychColorimetricData
---

\[T\_quantalAbsorptionsNormalized,T\_quantalAbsorptions,T\_quantalIsomerizations\] = ComputeRawConeFundamentals\(params,staticParams\)

Function to compute normalized cone quantal sensitivities
from underlying pieces and parameters.

Note that this routine returns quantal sensitivities.  You
may want energy sensitivities.  In that case, use EnergyToQuanta to convert
  T\_energy = EnergyToQuanta\(S,T\_quantal'\)'
and then renormalize.  \(You call EnergyToQuanta because you're converting
sensitivities, which go the opposite directoin from spectra.\)

The routine also returns two quantal sensitivity functions.  The first gives
the probability that a photon will be absorbed.  The second is the probability
that the photon will cause a photopigment isomerization.  It is the latter
that is what you want to compute isomerization rates from retinal illuminance.
See note at the end of function FillInPhotoreceptors for some information about
convention.  In particular, this routine takes pre\-retinal absorption into
account in its computation of probability of absorptions and isomerizations,
so that the relevant retinal illuminant is one computed without accounting for
those factors.  This routine does not account for light attenuation due to
the pupil, however.  The only use of pupil size here is becuase of its
slight effect on lens density as accounted for in the CIE standard.

In the passed params structure, you can either pass
the lambdaMax values for the photopigment, in which
case the absorbance is computed from the specified
nomogram, or you can pass the absorbance values
directly in T\_xxx format.  A typical choice in this
case would be 10.^T\_lgo10coneabsorbance\_ss for the
Stockman\-Sharpe/CIE estimates.

The typical use of this function is to be called by
ComputeCIEConeFundamentals, which sets up the
passed structures acording to the CIE standard.
This routine, however, could in principle be used
with a wide variety of choices of the component pieces.

The other place this function is used is in attempts to
fit a set of cone fundamentals by doing parameter search
over the pieces.  It is this second use that led to the
parameters being split over two separate structures, one
that is held static during the fit and the other which
contains the parameters that could be searched over by a calling
routine.  For examples, see:
  FitConeFundamentalsWithNomogram, FitConeFundamentalsTest.
Looking around today \(8/10/13\), I \(DHB\) don't see any examples where
this routine is called directly.  Rather, it is a subfunction
called by ComputeCIEConeFundamentals.  The search routines above
use ComputeCIEConeFundamentals, and only search over lambdaMax
values.  I think I wrote this with the thought that I might one
day search over more parameters, but lost motivation to carry it
throught.

The computations done here are very similar to those done in
routine FillInPhotoreceptors.  I \(DHB\) think that I forgot about
what FillInPhotoreceptors could do when I wrote this, which has
led to some redundancy. FillInPhotoreceptors returns a field
called effectiveAbsorptance, which are the actual quantal efficiencies
\(not normalized\) referred to the cornea.  FillInPhotoceptors also
computes a field isomerizationAbsorptance, which takes the quantal
efficiency of isomerizations \(probability of an isomerization given
an absorption into acount.  This routine does not do that.

It would probably be clever to unify the two sets of routines a
little more, but we may never get to it.  The routine ComputeCIEConeFundamentals
does contain a check that this routine and what is returned by FillInPhotoreceptors
agree with each other, for cases where the parameters match.

See also: ComputeCIEConeFundamentals, CIEConeFundamentalsTest, FitConeFundamentalsWithNomogram,
          FitConeFundamentalsTest, DefaultPhotoreceptors, FillInPhotoreceptors.

8/12/11  dhb  Starting to make this actually work.
8/14/11  dhb  Change name, expand comments.
8/10/13  dhb  [Expand](/docs/Expand) comments.  Return unscaled quantal efficiencies too.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetricData/ComputeRawConeFundamentals.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetricData/ComputeRawConeFundamentals.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetricData/ComputeRawConeFundamentals.m</code>
</div>
