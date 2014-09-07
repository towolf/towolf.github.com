---
layout: mfile
title: FontInfo
categories:
  - PsychBasic
encoding: UTF-8
---

numFonts=FontInfo('NumFonts');        % Return the number of installed fonts
fontInfoStructArray=FontInfo('Fonts');% Return an array of font info structs
versionInfo=FontInfo('Version');      % Return version info for Fonts command

# OS X

Return information about the text fonts installed on your computer.
FontInfo may be used in conjunction with [Screen](/docs/Screen)('DrawText') to select a
screen font which satifies your requirements.  FontInfo('Fonts') may omit
information in some fields of the returned struct, depending on what
information the font file itself supplies.  In particular, the
verticalMetrics and horizontalMetrics substructs are often empty.

The font number associated with a particular font may change if you
restart your computer or change the installed fonts.  Therefore you
should not code font  numbers into your scripts.  Instead, specify fonts
within your scripts by using font names.  You may pass font names
directly to [Screen](/docs/Screen)('TextFont'), or use the table returnd by the FontInfo
function to find the number of a font which satisfies your criteria for a
font.  Among those critera may be the font name itself.

# OS 9, WINDOWS, Linux

FontInfo does not exist on OS-9, Windows and Linux.
----

SEE ALSO: [Screen](/docs/Screen), [Screen](/docs/Screen)('TextFont')