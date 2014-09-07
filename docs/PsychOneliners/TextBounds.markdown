---
layout: mfile
title: TextBounds
categories:
  - PsychOneliners
---

bounds=TextBounds\(window,string\)

Returns the smallest enclosing rect for the drawn text, relative to
the current location. This bound is based on the actual pixels
drawn, so it incorporates effects of text smoothing, etc. "text"
may be a cell array or matrix of 1 or more strings. The strings are
drawn one on top of another, at the same initial position, before
the bounds are calculated. This returns the smallest box that will
contain all the strings. The prior contents of the scratch window
are lost. Usually it should be an offscreen window, so the user
won't see it. The scratch window should be at least twice as wide
and height as the text, because the text to cope with uncertainties
about text direction \(e.g. Hebrew\) and some unusual characters that extend
greatly to the left of their nominal starting point. If you only
know your nominal text size and number of characters, you might do
this to create your scratch window:

textSize=24;
string='Hello world.';
With 'w' being the handle of the onscreen window, e.g., w=[Screen](/docs/Screen)\('OpenWindow',0,0\);
woff=[Screen](/docs/Screen)\(w,'OpenOffscreenWindow',\[\],\[0 0 3\*textSize\*length\(string\) 2\*textSize\]\);
[Screen](/docs/Screen)\(woff,'TextFont','Arial'\);
[Screen](/docs/Screen)\(woff,'TextSize',textSize\);
[Screen](/docs/Screen)\(woff,'TextStyle',1\); % 0=plain \(default for new window\), 1=bold, etc.
bounds=TextBounds\(woff,string\);
...
[Screen](/docs/Screen)\(woff,'[Close](/docs/Close)'\);

The suggested window size in that call is generously large because there
aren't any guarantees from the font makers about how big the text might
be for a specified point size. Set your window's font, size, and
\(perhaps\) style before calling TextBounds.

Be warned that TextBounds and TextCenteredBounds are slow \(taking many
seconds\) if the window is large. They use the whole window, so if the
window is 1024x1204 they process a million pixels. The two slowest calls
are [Screen](/docs/Screen) 'GetImage' and FIND. Their processing time is proportional to
the number of pixels in the window.

OSX: Also see [Screen](/docs/Screen) 'TextBounds'.

The user interface would be cleaner if this function opened and closed
its own offscreen window, instead of writing in the user's window.
Unfortunately, this might cause some prohibitive overhead.

Also see TextCenteredBounds.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/TextBounds.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/TextBounds.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/TextBounds.m</code>
</div>
