---
layout: mfile
title: DrawMirroredTextDemo
categories:
  - PsychDemos
encoding: UTF-8
---

DrawMirroredTextDemo([upsideDown=0])
----

 Trivial example of drawing mirrored text. This demonstrates how to use
 low-level OpenGL API functions to apply geometric transformations to
 the drawn objects.

 Will draw a text string, once in normal orientation, and once mirrored.
 The mirrored text is either mirrored left\<-\>right, or upside down if you
 set the optional 'upsideDown' flag to 1. At each key press, the text
 will be redrawn at an increasing size, until after a couple of redraws
 the demo will end.

 The demo also draws a bounding box around the text string to demonstrate
 how you can find out about the bounds of a text string via
 [Screen](/docs/Screen)('TextBounds').

 The mirroring is implemented by first defining a geomtric transformation
 which will apply to all further drawn shapes and text strings. Then the
 text string is drawn via [Screen](/docs/Screen)('DrawText') -- thereby affected by the
 geometric transform. Then the transform is undone to "normal".

 How does this work?

 1\. The command [Screen](/docs/Screen)('glPushMatrix'); makes a "backup copy" of the
 current transformation state -- the default way of drawing.

 2\. The command [Screen](/docs/Screen)('glTranslate', w, xc, yc, 0); translates the
 origin of the coordinate system (which is normally located at the
 upper-left corner of the screen) into the geometric center of the
 location of the text string. We find the center xc,yc by retrieving the
 bounding box of the text string [Screen](/docs/Screen)('TextBounds'), then calculating
 the center of that box [xc, yc].

 3\. The [Screen](/docs/Screen)('glScale', w, x, y, z); will scale all further drawn
 objects by a factor 'x' in x-direction (horizontal), 'y' in y-direction
 (vertical), 'z' in z-direction (depths). Scaling happen with respect to
 the current origin. As we just set the origin to be the center of the
 text string in step 2, the object will "scale" around that point. A
 value of -1 effectively switches the direction along the 'x' axis for a
 horizontal flip, or along the 'y' axis for an upside down vertical flip.
 Values with a magnitude other than 1 would scale the whole text up or
 down in size.

 4\. The command [Screen](/docs/Screen)('glTranslate', w, -xc, -yc, 0); translates the
 origin of the coordinate system back to the upper-left corner of the
 screen. This to make sure that all coordinates provided later on are
 wrt. to the usual reference frame.

 Steps 2,3 and 4 are internally merged to one mathematical transformation:
 The flipping of all drawn shapes and objects around the screen position
 [xc,yc] -- the center of the text string.

 5\. We [Screen](/docs/Screen)('DrawText') the text string --\> The flipping applies.

 6\. We undo the whole transformation via [Screen](/docs/Screen)('glPopMatrix') thereby
 restoring the original "do nothing" transformation from the backup copy
 which was created in step 1. All further drawing is therbey unaffected
 by the flipping, so we can draw the second copy of the text and the
 bounding box.

Besides the scaling and translation transform for moving, rescaling and
flipping drawn objects and shapes, there is also the [Screen](/docs/Screen)('glRotate')
transform to apply rotation around axis.

This transformations apply to any drawing command, not only text strings!
----

see also: PsychDemos