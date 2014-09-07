---
layout: mfile
title: ClockRandSeed
categories:
  - PsychProbability
encoding: UTF-8
---

[seed,whichGen] = ClockRandSeed([seed],[whichGen])  

ClockRandSeed seeds the random number from the time-of-day clock. If seed  
is passed this is used instead.  

The multiplier 1e6 in fix(1e6\*sum(clock)) is bigger than the 100  
suggested by Mathworks (see help RAND).  They suggest 100\*sum(clock), but  
this would only change the seed once every 1/100 sec, which might  
correspond to many iterations of a loop. With the bigger  multiplier it's  
pretty sure (depending only on clock grain) that two successive calls  
will generate different seeds.  

Also unlike the Mathworks suggestion (see help RAND), we call FIX. This  
has no effect on RAND and RANDN, but makes it easier to correctly print  
the seed to a file. When a random seed generates an interesting result  
one would like to be able to recreate the conditions that generated the  
run. If the seed 1e6\*sum(clock) is printed to a file, '%.0f' will often  
round it differently than RAND would.  

Note in that in Matlab 5 there are two random number generators, the  
Matlab 5 generator and the Matlab 4 generator.  (Matlab 4  
has only the version 4 generator.)  ClockRandSeed checks what version of  
Matlab you're running and uses the version 5 generator if it can.  The  
string whichGen contains 'seed' for the version 4 generator and 'state'  
for the version 5 generator.  

See also: rand, randn.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychProbability/ClockRandSeed.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychProbability/ClockRandSeed.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychProbability/ClockRandSeed.m</code>
</div>
