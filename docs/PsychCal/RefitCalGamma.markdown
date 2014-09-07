---
layout: mfile
title: RefitCalGamma
categories:
  - PsychCal
encoding: UTF-8
---

RefitCalGamma

Refit the gamma data from a calibration.

See also CalDemo, CalibrateFitGamma, SetGammaMethod, GamutToSettings

3/27/02  dhb  Wrote it.
8/26/03  dhb, jl  Allow changing dacsize of calibraiton.  Useful for dropping from 10 to 8.
2/2/05   dhb, dam [Ask](/docs/Ask) for filename to save to, rather than automatically overwrite.
9/26/08  dhb, ijk, tyl  Simplify naming possibilities.  Add some better help.
9/27/08  dhb      Fix up dacsize fitting.
                  Clearer prompts (show default values).
11/19/09 dhb      Added crtSumPow option.  This works great for our FrontRoom monitor, which
                  was not well fit by the traditional gamma model.  The work is done in
                  function CalibrateFitGamma.  See comments there.
11/20/09 dhb      More terms in crtSumPow.
3/07/10  dhb      Call CalibrateFitLinMod as well.
3/08/10  dhb      Update list of fit type options.
5/28/10  dhb      Add yoked fitting routine to calls.  Should have no effect when yoked isn't set, but do the right thing when it is.
6/5/10   dhb      Update type list provided to user.
         dhb      Better plots, using plot subroutines.
5/26/12  dhb      Added ability to use raw measured data as the fit gamma table.  See comment where that's done below.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychCal/RefitCalGamma.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychCal/RefitCalGamma.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychCal/RefitCalGamma.m</code>
</div>
