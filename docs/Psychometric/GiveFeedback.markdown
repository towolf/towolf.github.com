---
layout: mfile
title: GiveFeedback
categories:
  - Psychometric
encoding: UTF-8
---

 GiveFeedback(correct)

 Give auditory feedback about correctness of respose.  One beep for
 correct, two beeps for incorrect.  Some labs (e.g. dgp) prefer
 a short beep for correct, no sound for incorrect.  One could
 easily add a flag to this routine to allow this behavior.

 3/5/97     dhb  Wrote it
 1/25/00    emw  Added platform conditionals
 3/8/2000   dgp  Fixed platform conditionals
 4/14/00   dhb  Fix call to [Snd](/docs/Snd) for windows.
 4/13/02    dgp  Eliminate obsolete calls to SndPlay. Just call [Snd](/docs/Snd) on both platforms.
                 It's important to specify the sample rate, because the default is
                 platform-dependent.
 11/15/03  dhb  Wait for sound to complete before returning.  Failure to do so
                 was causing problems when [Snd](/docs/Snd)('[Close](/docs/Close)') was called by calling
                 routine.