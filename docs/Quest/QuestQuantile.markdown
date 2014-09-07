---
layout: mfile
title: QuestQuantile
categories:
  - Quest
encoding: UTF-8
---

intensity=QuestQuantile(q,[quantileOrder])

Gets a quantile of the pdf in the struct q. You may specify the desired
quantileOrder, e.g. 0.5 for median, or, making two calls, 0.05 and 0.95
for a 90% confidence interval. If the "quantileOrder" argument is not
supplied, then it's taken from the "q" struct. QuestCreate uses
QuestRecompute to compute the optimal quantileOrder and saves that in the
"q" struct; this quantileOrder yields a quantile  that is the most
informative intensity for the next trial.

This is based on work presented at a conference, but otherwise unpublished:
Pelli, D. G. (1987). The ideal psychometric procedure. Investigative
Ophthalmology & Visual Science, 28(Suppl), 366.

See Quest.