---
layout: mfile
title: TextCenteredBounds
categories:
  - PsychOneliners
encoding: UTF-8
---

bounds=TextCenteredBounds\(window,text\)

Returns the smallest enclosing rect for the drawn text, relative to the
current location. This bound is based on the actual pixels drawn, so it
incorporates effects of text smoothing, etc. All text is drawn on the
same baseline, horizontally centered by using the x offset
-[Screen](/docs/Screen)\(w,'TextWidth',string\)/2. "text" may be a cell array or matrix of
1 or more strings. The strings are drawn one on top of another, all
horizontally centered at the current position, before the bounds are
calculated. This returns the smallest box that will contain all the
strings. The prior contents of the scratch window are lost. Usually it
should be an offscreen window, so the user won't see it. If you only
know your nominal text size and number of characters, you might do this

w=[Screen](/docs/Screen)\(-1,'OpenOffscreenWindow',\[\],\[0 0 1.5\*textSize\*length\(string\) 2\*textSize\],1\);

The suggested window size in that call is generously large because there
aren't any guarantees from the font makers about how big the text might
be for a specified point size. The pixelSize of 1 \(the last argument\)
minimizes the memory requirements.

Be warned that TextBounds and TextCenteredBounds are slow \(taking many
seconds\) if the window is large. They use the whole window, so if the
window is 1024x1204 they process a million pixels. The two slowest calls
are [Screen](/docs/Screen) 'GetImage' and FIND. Their processing time is proportional to
the number of pixels in the window. We haven't checked, but it's very
likely that processing time is also proportional to pixel size, so we
suggest using a small pixel size \(e.g. 1 bit, using an offscreen
window\).

The user interface would be cleaner if this function opened and closed
its own offscreen window, without bothering the user. Unfortunately the Mac
OS takes on the order of a second to open and to close an offscreen
window, making the overhead prohibitive.

Also see TextBounds and [Screen](/docs/Screen) 'TextWidth' and 'DrawText'.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/TextCenteredBounds.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/TextCenteredBounds.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/TextCenteredBounds.m</code>
</div>
