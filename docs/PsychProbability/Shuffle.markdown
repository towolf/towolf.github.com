---
layout: mfile
title: Shuffle
categories:
  - PsychProbability
encoding: UTF-8
---

 [Y,index] = [Shuffle](/docs/Shuffle)(X)

 Randomly sorts X.
 If X is a vector, sorts all of X, so Y = X(index).
 If X is an m-by-n matrix, sorts each column of X, so
    for j=1:n, Y(:,j)=X(index(:,j),j).

 Also see SORT, [Sample](/docs/Sample), [Randi](/docs/Randi), and RandSample.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychProbability/Shuffle.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychProbability/Shuffle.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychProbability/Shuffle.m</code>
</div>
