---
layout: mfile
title: DefaultPhotoreceptors
categories:
  - PsychColorimetricData
encoding: UTF-8
---

photoreceptors = DefaultPhotoreceptors\(kind\)

Return a structure containing default sources
for photoreceptor complements of various kinds.

Available kinds
  LivingHumanFovea \(Default\) - Human foveal cones in the eye
  LivingHumanMelanopsinTsujimura2010 - Estimate of melanopsin gc spectral sensitivity in living eye
  LivingDog - Canine
  GuineaPig - Guinea pig in dish

See also:  FillInPhotoreceptors, PrintPhotoreceptors, RetIrradianceToIsoRecSec
 IsomerizationsInEyeDemo, IsomerizationsInDishDemo, ComputeCIEConeFundamentals,
 RodFundamentalTest, MelanopsinFundamentalTest.

NOTES: Should probably update the parameters for LivingHumanFovea so that
they produce the Stockman-Sharpe fundamentals.  This should be pretty
straightforward, now that all the pieces are implemented as via ComputeCIEConeFundamentals.

7/25/03  dhb  Wrote it.
12/04/07 dhb  Added dog parameters
8/14/11  dhb  Added fieldSizeDegrees and ageInYears fields to photoreceptors for LivingHumanFovea case.
              These defaults match the CIE standard.
4/20/12  dhb  Add LivingHumanMelanopsin
5/10/12  dhb  Changed name for LivingHumanMelanopsin to postpend Tsujimura2010
8/12/13  dhb  Change field order to make printouts look nicer.
11/13/13 dhb  Add 'LivingHumanRod' and 'LivingHumanMelanopsin' options.
5/26/14  dhb  Add pupilDimater.value = \[\] to fix FillInPhotoreceptors.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetricData/DefaultPhotoreceptors.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetricData/DefaultPhotoreceptors.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetricData/DefaultPhotoreceptors.m</code>
</div>
