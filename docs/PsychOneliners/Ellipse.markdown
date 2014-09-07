---
layout: mfile
title: Ellipse
categories:
  - PsychOneliners
encoding: UTF-8
---

[Ellipse](/docs/Ellipse)(a) creates a [Circle](/docs/Circle) with
diameter == ceil(2\*a)

[Ellipse](/docs/Ellipse)(a,b) creates an [Ellipse](/docs/Ellipse) with
horizontal axis == ceil(2\*a) and vertical axis == ceil(2\*b)

[Ellipse](/docs/Ellipse)(a,b,power) generates a superEllipse according to the
geometric formula (x./a).^power + (y./b).^power \< 1

[Ellipse](/docs/Ellipse)(a,b,horpow,verpow) generates a generalized superEllipse according
to the geometric formula(x./a).^horpow + (y./b).^verpow \< 1

For more info on superEllipses, see
  http://en.wikipedia.org/wiki/SuperEllipse

[Ellipse](/docs/Ellipse) returns a (tighly-fitting) boolean matrix which is true for all
points on the surface of the [Ellipse](/docs/Ellipse) and false elsewhere