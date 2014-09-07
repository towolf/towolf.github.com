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