---
layout: mfile
title: DrawFormattedText
categories:
  - PsychBasic
---

\[nx, ny, textbounds\] = DrawFormattedText\(win, tstring \[, sx\]\[, sy\]\[, color\]\[, wrapat\]\[, flipHorizontal\]\[, flipVertical\]\[, vSpacing\]\[, righttoleft\]\[, winRect\]\)

Draws a string of text 'tstring' into Psychtoolbox window 'win'. Allows
some basic formatting. The text string 'tstring' may contain newline
characters '\\n'. Whenever a newline character '\\n' is encountered, a
linefeed and carriage return is performed, breaking the text string into
lines. 'sx' defines the left border of the text: If it is left out, text
starts at x\-position zero, otherwise it starts at the specified position
'sx'. If sx=='center', then each line of text is horizontally centered in
the window. If sx=='right', then each line of text is right justified to
the right border of the target window, or of 'winRect' if provided. 'sy'
defines the top border of the text. If left out, it starts at the top of
the window, otherwise it starts at the specified vertical pixel position.
If sy=='center', then the whole text is vertically centered in the
window. 'color' is the color value of the text \(color index or \[r g b\]
triplet or \[r g b a\] quadruple\). If color is left out, the current text
color from previous text drawing commands is used. 'wrapat', if provided,
will automatically break text strings longer than 'wrapat' characters
into newline separated strings of roughly 'wrapat' characters. This is
done by calling the WrapString function \(See 'help WrapString'\). 'wrapat'
mode may not work reliably with non\-ASCII text strings, e.g., UTF\-8
encoded uint8 strings on all systems.

The optional flag 'flipHorizontal' if set to 1 will mirror the text
horizontally, whereas the optional flag 'flipVertical' if set to 1 will
mirror the text vertically \(upside down\).

The optional argument 'vSpacing' sets the spacing between the lines. Default
value is 1.

The optional argument 'righttoleft' if set to 1, will ask to draw the
text string in right\-to\-left reading direction, e.g., for scripts which
read right to left

The optional argument 'winRect' allows to specify a \[left top right bottom\]
rectange, in which the text should be centered/placed etc. By default,
the rectangle of the whole 'win'dow is used.

The function employs clipping by default. Text lines that are detected as
lying completely outside the 'win'dow or optional 'winRect' will not be
drawn, but clipped away. This allows to draw multi\-page text \(multiple
screen heights\) without too much loss of drawing speed. If you find the
clipping to interfere with text layout of exotic texts/fonts at exotic
sizes and formatting, you can define the global variable...

global ptb\_drawformattedtext\_disableClipping;
... and set it like this ...
ptb\_drawformattedtext\_disableClipping = 1;
... to disable the clipping.

Clipping also gets disabled if you request the optional 3rd return
parameter 'textbounds' to ensure correct computation of a bounding box
that covers the complete text. You can enforce clipping by setting
ptb\_drawformattedtext\_disableClipping = \-1; however, computed bounding
boxes will then only describe the currently visible \(non\-clipped\) text.


The function returns the new \(nx, ny\) position of the text drawing cursor
and the bounding rectangle 'textbounds' of the drawn string. \(nx,ny\) can
be used as new start position for connecting further text strings to the
bottom of the drawn text string. Calculation of these bounds is
approximative, so it may give wrong results with some text fonts and
styles on some operating systems.

See DrawFormattedTextDemo for a usage example.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/DrawFormattedText.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/DrawFormattedText.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/DrawFormattedText.m</code>
</div>
