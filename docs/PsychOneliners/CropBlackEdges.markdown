---
layout: mfile
title: CropBlackEdges
categories:
  - PsychOneliners
encoding: UTF-8
---

coords = croblackedges(image)
returns coordinates that can be used to cut the black edges from an image
the trick is to sum the image in the x-direction and find where the sum
is zero, then you know where there are black edges above and below the
image; same trick for the edges left and right by summing in the
y-direction.

COORDS = [xmin xmax ymin ymax]

to cut the edges use:
cutimage = image(coords(3):coords(4),coords(1):coords(2));

DN 2007       Wrote it
DN 2008-07-30 Now returns correct indices if one or more or all sides of
              the image do not have a black edge
DN 2009-02-02 Now returns error msg if all is black