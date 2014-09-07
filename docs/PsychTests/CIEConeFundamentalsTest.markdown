---
layout: mfile
title: CIEConeFundamentalsTest
categories:
  - PsychTests
encoding: UTF-8
---

CIEConeFundamentalsTest  

This program tests the fit cones routine, and demonstrates its use.  

The goal here is to find parameters that reproduce a set of cone  
fundamentals from their underlying parts.  That would then let  
one vary the parameters of the parts, to get different theoretically  
specfied cone fundamentals.  

This shows that the standard does an excellent job of reconstructing  
the Stockman/Sharpe 2-degree and 10 degree fundamentals if one starts  
with the tabulated LMS absorbances.  The agreement is less perfect  
if one uses the nomogram and recommended lambda-max values to  
generate the absorbances.  See comment on this point in StockmanSharpeNomogram.m  

The code here is closely related (and uses) a more general set of code  
for setting parameters for photoreceptors and computing quantal  
sensitivities. See:  
   DefaultPhotoreceptors, FillInPhotoreceptors, PrintPhotoreceptors,IsomerizationsInDishDemo  
   IsomerizationsInEyeDemo, ComputeCIEConeFundamentals, ComputeRawConeFundamentals.  

8/11/11  dhb  Wrote it  
8/14/11  dhb  Clean up a little.  
12/16/12 dhb  Added test for rods.  
08/10/13 dhb  Better integration with the photoreceptor struct code.  
03/14/14 dhb  Add Smith-Pokorny to 2 degree plot, for comparison.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychTests/CIEConeFundamentalsTest.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychTests/CIEConeFundamentalsTest.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychTests/CIEConeFundamentalsTest.m</code>
</div>
