---
layout: mfile
title: PredictVisualOnsetForTime
categories:
  - PsychBasic
---

tonset = PredictVisualOnsetForTime\(window, when \[, refreshinterval\]\)

Map a specific requested 'when' visual onset time, as you would pass it as
'when' parameter to [Screen](/docs/Screen)\('[Flip](/docs/Flip)', window, when\); to the estimated onset
time of the "flipped" stimulus.

By default, the refresh interval from [Screen](/docs/Screen)\('GetFlipInterval', window\);
is used for calculation, but you can provide an optional
'refreshinterval' to override this choice.

This function predicts the real onset time of your "flipped" stimulus,
taking into account that [Screen](/docs/Screen)\('[Flip](/docs/Flip)'\) will not show your stimulus at
exactly the requested 'when' time, but it will synchronize stimulus onset
to the display refresh cycle of your monitor, ie, it will wait for onset
of the closest vertical blanking interval equal or later than 'when'.

You can use the predicted 'tonset' to synchronize other modalities to
visual stimulus onset. E.g., our sound driver PsychPortAudio can accept
such a time as sound onset deadline in order to synch sound onset with
visual stimulus onset...

Of course if your stimulus is too complex to be finished with drawing
until 'when' then [Screen](/docs/Screen)\('[Flip](/docs/Flip)'\) will miss the deadline and this
prediction will be wrong.

# Accuracy of prediction:

On systems that support timing via beamposition queries, the prediction
should be accurate to better than 200 microseconds. On systems without
beamposition queries, the prediction may be off by up to a millisecond
worst case. On such systems we can't determine and correct for the
duration of the vertical blanking interval, so the prediction will be a
bit too early.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/PredictVisualOnsetForTime.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/PredictVisualOnsetForTime.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/PredictVisualOnsetForTime.m</code>
</div>
