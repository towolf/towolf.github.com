---
layout: mfile
title: ValetonVanNorrenParams
categories:
  - PsychColorimetricData
encoding: UTF-8
---

[params] = ValetonVanNorrenParams(logIsoRate,[photoreceptors],[trolandType],[LMRatio])

Return a structure containting the parameters of the
Valeton and VanNorren model of cone adaptation
as a function of the number of isomerizations per cone per
second.  The structure also contains the table of trolands
and corresponding isomerization rates used to spline the
published numbers.

Valeton and Van Norren (1983, Vision Research, pp. 1539-1547)
provide their parameters as a function of the number of trolands
incident on their monkey retina.  We convert this to isomerizations
per cone, so that we can work in more interesting physical units.

The conversion involves making assumptions about a lot of constants.
The assumptions are encapsulated by the photoreceptors structure
and the passed eye length source and troland type.

  photoreceptors - structure interpreted by RetIrradianceToIsoRecSec.
  eyeLengthSource - string or value interpreted by EyeLength.
  trolandType - string interpreted by TrolandsToRetIrradiance.
  LMRatio - value of L to M cone ratio to assume for original measurements (Default 2).

The parameters are provided in Table 1 of the paper, for a range
of troland values.  The model parameters are sigmaL and gamma.
and gamma.

See also: TrolandsToRetIrradiance, RetIrradianceToIsoRecSec, EyeLength,
  DefaultPhotoreceptors, FillInPhotoreceptors.

\7/18/03  dhb  Started writing it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetricData/ValetonVanNorrenParams.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetricData/ValetonVanNorrenParams.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetricData/ValetonVanNorrenParams.m</code>
</div>
