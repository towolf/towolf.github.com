---
layout: mfile
title: ComputeCIEConeFundamentals
categories:
  - PsychColorimetricData
encoding: UTF-8
---

[T\_quantalAbsorptionsNormalized,T\_quantalAbsorptions,T\_quantalIsomerizations] = ComputeCIEConeFundamentals(S,fieldSizeDegrees,ageInYears,pupilDiameterMM,[lambdaMax],[whichNomogram],[LserWeight],[DORODS],[rodAxialDensity],[fractionPigmentBleached])

Function to compute normalized cone quantal sensitivities
from underlying pieces, as specified in CIE 170-1:2006.

IMPORTANT: This routine returns quantal sensitivities.  You
may want energy sensitivities.  In that case, use EnergyToQuanta to convert
  T\_energy = EnergyToQuanta(S,T\_quantal')'
and then renormalize.  (You call EnergyToQuanta because you're converting
sensitivities, which go the opposite directoin from spectra.)
The routine also returns two quantal sensitivity functions.  The first gives
the probability that a photon will be absorbed.  The second is the probability
that the photon will cause a photopigment isomerization.  It is the latter
that is what you want to compute isomerization rates from retinal illuminance.
See note at the end of function FillInPhotoreceptors for some information about
convention.  In particular, this routine takes pre-retinal absorption into
account in its computation of probability of absorptions and isomerizations,
so that the relevant retinal illuminant is one computed without accounting for
those factors.  This routine does not account for light attenuation due to
the pupil, however.  The only use of pupil size here is becuase of its
slight effect on lens density as accounted for in the CIE standard.

This standard allows customizing the fundamentals for
field size, observer age, and pupil size in mm.

To get the Stockman-Sharpe/CIE 2-deg fundamentals, use
  fieldSizeDegrees = 2;
  ageInYears = 32;
  pupilDiameterMM = 3;
and don't pass the rest of the arguments.

To get the Stockman-Sharpe/CIE 10-deg fundamentals, use
  fieldSizeDegrees = 10;
  ageInYears = 32;
  pupilDiameterMM = 3;
and don't pass the rest of the arguments.

Although this routine will compute something over any wavelength
range, I'd (DHB) recommend not going lower than 390 or above about 780 without
thinking hard about how various pieces were extrapolated out of the range
that they are specified in the standard.  Indeed, the lens optical
density measurements only go down to 400 nm and these are extropolated
to go below 400.

This routine will compute from tabulated absorbance or absorbance based on a nomogram, where
whichNomogram can be any source understood by the routine PhotopigmentNomogram.  To obtain
the nomogram behavior, pass a lambdaMax vector. You can then also optionally pass a nomogram
source (default: StockmanSharpe).

The nominal values of lambdaMax to fit the CIE 2-degree fundamentals with the
Stockman-Sharpe nomogram are 558.9, 530.3, and 420.7 nm for the LMS cones respectively.
These in fact do a reasonable job of reconstructing the CIE 2-degree fundamentals, although
there are small deviations from what you get if you simply read in the tabulated cone
absorbances.  Thus starting with these as nominal values and shifting is a reasonable way to
produce fundamentals tailored to observers with different known photopigments.

Relevant to that enterprise, S & S (2000) estimate the wavelength difference
between the ser/ala variants to be be 2.7 nm (ser longer).

If you pass lambaMax and its length is 4, then first two values are treated as
the peak wavelengths of the ser/ala variants of the L cone pigment, and these
are then weighted according to LserWeight and (1-LserWeight).  The default
for LserWeight is 0.56.  After travelling it for a distance to try to get better
agreement between the nomogram based fundamentals and the tabulated fundamentals
I (DHB) gave up and decided that using a single lambdaMax is as good as anything
else I could come up with. If you are interested, see FitConeFundametnalsTest.

This function also has an option to compute rod spectral sensitivities, using
the pre-retinal values that come from the CIE standard.  Set DORODS to true on
call.  You then need to explicitly pass a single lambdaMax value.  You can
also pass an optional rodAxialDensity value.  If you don't pass that, the
routine uses the 'Alpern' estimate for 'Human'/'Rod' embodied in routine
PhotopigmentAxialDensity.  The default nomogram for the rod spectral
absorbance is 'StockmanSharpe', but you can override with any of the
others available in routine PhotopigmentNomogram.  Use of this requires
good choices for lambdaMax, rodAxialDensity, and the nomogram.  We are
working on identifying those values more precisely.

Finally, you can adjust the returned spectral sensitivities to account for
the possibility that some of the pigment in the cones is bleached.  Pass
a column vector with same length as number of spectral sensitivities being
computed.  You need to estimate the fraction elsewhere.

See also: ComputeRawConeFundamentals, CIEConeFundamentalsTest,
FitConeFundamentalsTest, FitConeFundamentalsWithNomogram, StockmanSharpeNomogram,
ComputePhotopigmentBleaching.

8/13/11  dhb  Wrote it.
8/14/11  dhb  Clean up a little.
12/16/12 dhb, ms  Add rod option.
08/10/13 dhb  Test for consistency between what's returned by FillInPhotoreceptors and
              what's returned by ComputeRawConeFundamentals.
05/24/14 dhb  Add fractionPigmentBleached optional arg.
05/26/14 dhb  Comment improvements.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetricData/ComputeCIEConeFundamentals.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetricData/ComputeCIEConeFundamentals.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetricData/ComputeCIEConeFundamentals.m</code>
</div>
