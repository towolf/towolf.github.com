---
layout: mfile
title: Sample
categories:
  - PsychProbability
encoding: UTF-8
---

 [Y,index] = [Sample](/docs/Sample)(X)

 Returns a random sample from X.
 If X is a vector, returns a scalar sample from X, so Y = X(index).
 If X is an m-by-n matrix, m\>1 && n\>1, samples each column of X:
    for j=1:n, Y(j)=X(index(j),j).

 Also see RandSample, [Shuffle](/docs/Shuffle), SORT, and [Randi](/docs/Randi).