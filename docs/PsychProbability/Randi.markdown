---
layout: mfile
title: Randi
categories:
  - PsychProbability
encoding: UTF-8
---

i=[Randi](/docs/Randi)(n,[dims])
Returns a random integer sample from 1:n. The optional second argument
may be used to specify the size of the returned array of independent
samples. E.g. randi(100,[3,3]) returns a 3x3 array of independent samples
drawn from the range 1:100. Also see RAND, RANDN, RandSample, [Sample](/docs/Sample), and
[Shuffle](/docs/Shuffle).

We assume that n is a positive integer, and rely on the fact that RAND
never returns 0 or 1.

[Randi](/docs/Randi)(n) is similar to David Brainard's [Ranint](/docs/Ranint)(n).