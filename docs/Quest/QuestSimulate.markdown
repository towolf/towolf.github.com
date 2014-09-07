---
layout: mfile
title: QuestSimulate
categories:
  - Quest
encoding: UTF-8
---

response=QuestSimulate(q,intensity,tActual [,plotIt])

Simulate the response of an observer with threshold tActual when exposed
to a stimulus tTest.

'plotIt' is optional: If set to a non-zero value, the simulated Quest
session is visualized in a plot which shows the psychometric function of
the simulated observer, where Quest placed test trials and what the
observers response was. plotIt == 1 shows past trials in black, the
current trial in green or red for a positive or negative response. plotIt
\== 2 color-codes all trials in red/green for negative or positive
responses. By default, nothing is plotted.

See Quest.