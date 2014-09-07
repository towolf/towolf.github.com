---
layout: mfile
title: MultiNormalDraw
categories:
  - PsychProbability
encoding: UTF-8
---

x = MultiNormalDraw(n,u,K)

Make n multivariate normal draws with mean u and covariance matrix K.
Each draw is in a single column of y, which has n columns.

The routine operates by computing the appropriate linear transformation
of a N(0,I) multivariate normal draw.  This transformation is given by
y= C'x + u where K = C'C.  This works because the covariance of a
distribution y = Cx is in general given by Ky = C Kx C'.  In our case
Kx= I so Ky = C'C = K.

K = 0 is handled as a special case