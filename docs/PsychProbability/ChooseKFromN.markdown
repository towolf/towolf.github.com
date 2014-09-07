---
layout: mfile
title: ChooseKFromN
categories:
  - PsychProbability
encoding: UTF-8
---

 choice = ChooseKFromN(n,k,[unique])

 Choose k distinct integers out of n.   The indices come back in
 randomized order if unique is absent or 0.  They come back
 sorted if unique is equal to 1.

 4/11/94    dhb     Wrote it.
 2/8/98    dhb     Renamed to avoid name conflict with Matlab 5 nchoosek.m
            dhb     Eliminate obsolete call to rand('uniform').
 7/24/04   awi     Cosmetic.
 1/29/05   dgp     Cosmetic.