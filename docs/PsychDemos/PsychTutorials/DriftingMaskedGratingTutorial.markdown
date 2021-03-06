---
layout: mfile
title: DriftingMaskedGratingTutorial
categories:
  - PsychTutorials
encoding: UTF-8
---

function DriftDemo2(angle, cyclespersecond, f, drawmask)
----

Display an animated grating using the new [Screen](/docs/Screen)('DrawTexture') command.
In the OS X Psychtoolbox [Screen](/docs/Screen)('DrawTexture') replaces
[Screen](/docs/Screen)('CopyWindow'). The demo will stop after roughly 20 seconds have
passed or after the user hits a key.

This demo illustrates how to draw an animated grating online by use of
only one grating texture. We create one texture with a static sine
grating. In each successive frame we only draw a rectangular subregion of
the sine-texture onto the screen, basically showing the texture through
an aperture. The subregion - and therefore our "aperture" is shifted each
frame, so we create the impression of a moving grating.

The demo also shows how to use alpha-blending for masking the grating
with a gaussian transparency mask (a texture with transparency layer).

And finally, we demonstrate rotated drawing, as well as how to emulate
the old OS-9 'WaitBlanking' command with the new '[Flip](/docs/Flip)' command.

# Parameters:

angle = Angle of the grating with respect to the vertical direction.
cyclespersecond = Speed of grating in cycles per second.
f = Frequency of grating in cycles per pixel.
drawmask = If set to 1, then a gaussian aperture is drawn over the grating

# CopyWindow vs. DrawTexture:

In the OS 9 Psychtoolbox, [Screen](/docs/Screen) ('CopyWindow") was used for all
time-critical display of images, in particular for display of the movie
frames in animated stimuli. In contrast, [Screen](/docs/Screen)('DrawTexture') should not
be used for display of all graphic elements,  but only for  display of
MATLAB matrices.  For all other graphical elements, such as lines,  rectangles,
and ovals we recommend that these be drawn directly to the  display
window during the animation rather than rendered to offscreen  windows
prior to the animation.
----

see also: PsychDemos, MovieDemo