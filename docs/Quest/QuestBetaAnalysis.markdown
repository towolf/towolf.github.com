---
layout: mfile
title: QuestBetaAnalysis
categories:
  - Quest
encoding: UTF-8
---

betaEstimate=QuestBetaAnalysis(q,[fid]);

Analyzes the quest function with beta as a free parameter. It prints (in
the file or files pointed to by fid) the mean estimates of alpha (as
logC) and beta. Gamma is left at whatever value the user fixed it at.

Note that normalization of the pdf, by QuestRecompute, is disabled because it
would need to be done across the whole q vector. Without normalization,
the pdf tends to underflow at around 1000 trials. You will have some warning
of this because the printout mentions any values of beta that were dropped
because they had zero probability. Thus you should keep the number of trials
under around 1000, to avoid the zero-probability warnings.

See Quest.