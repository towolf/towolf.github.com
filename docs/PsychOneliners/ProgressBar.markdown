---
layout: mfile
title: ProgressBar
categories:
  - PsychOneliners
encoding: UTF-8
---

ProgressBar    Ascii progress bar.
   progBar = ProgressBar(nMax,str) creates a progress bar and returns a
   pointer to a function handle which can then be called to update it.

   To update, call progBar(currentStep)

   Example:
      n = 500;
      progBar = ProgressBar(n,'computing...');
      for tmp = 1:n
        progBar(tmp);
        pause(.01)
      end