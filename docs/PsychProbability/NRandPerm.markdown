---
layout: mfile
title: NRandPerm
categories:
  - PsychProbability
encoding: UTF-8
---

NRandPerm Random permutation.  
   NRandPerm(n,nret) is a random permutation of the integers from 1 to n,  
   of which nret elements are returned.  
   NRandPerm thus returns a random selection of integers from 1 to n with  
   no repeats.  

   For example, NRandPerm(6,4) might be [2 4 5 6].  

   Note that NRandPerm calls RAND and therefore changes RAND's state.  

   See also PERMUTE, RANDPERM.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychProbability/NRandPerm.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychProbability/NRandPerm.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychProbability/NRandPerm.m</code>
</div>
