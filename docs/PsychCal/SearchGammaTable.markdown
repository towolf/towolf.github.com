---
layout: mfile
title: SearchGammaTable
categories:
  - PsychCal
encoding: UTF-8
---

 values = SearchGammaTable(targets, input, table)

 Return the [0-1] entry from the passed table that produces
 output closest to the [0-1] target.

 The targets are assumed to be a row vector.
 The table is assumed to be a column vector.
 The returned indices and values are are row vectors.

 Works by using Matlab's interp1, with the output as the x values and
 the input as the f(x) values.

 I suspect that this is a fast Matlab implementation, but those who want
 to try are welcome to try to do better.  (Remember, though, that this
 routine gains in efficiency the more searches are done at once.
 This is because it contains no dreaded loops.)

 \4/2/94     dhb     Added code that checks for special case of zero output.
 \4/4/94     dhb     Fixed code added on 4/2.
 \4/5/94     jms     Fixed code added on 4/2.
 \1/21/95        dhb     Write search as a loop.  Loses time and elegance,
                        but prevents allocation of arrays that may be huge.
 \11/16/06      dhb     Renamed as SearchGammaTable.
               dhb     Start work on converting to [0-1] universe.  Change
                       name and interface.
 \11/20/06      dhb     Finish update by calling through MATLAB's interpolation function.
 \9/15/08       dhb     Handle case where there are a bunch of zeros at the beginning of gamma table.
 \5/26/12       dhb     Improve comment.  This was not doing exhaustive search.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychCal/SearchGammaTable.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychCal/SearchGammaTable.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychCal/SearchGammaTable.m</code>
</div>
