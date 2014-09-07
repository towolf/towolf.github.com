---
layout: mfile
title: IsomerizationsFromAbsorptions
categories:
  - PsychColorimetric
encoding: UTF-8
---

 [isomerizationRate] = IsomerizationsFromAbsorptions(photonAbsorptionRate,[quantalEfficiency])

    Compute isomerization rate, R\* per photreceptor per sec, given
 photon absorption rate and photopgiment quantal efficiency.

 Default value for quantalEfficiency is inherited from PhotopigmentQuantalEfficiency
 called with type 'Generic'.

 06/11/03 lyin      Rewrote it.
 06/23/03 dhb       Change name, made quantalEfficiency an argument.
 07/25/03 dhb    Take default value from data routine.