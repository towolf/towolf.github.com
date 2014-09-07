---
layout: mfile
title: MonitorGammaError
categories:
  - PsychGamma
encoding: UTF-8
---

err=MonitorGammaError(p,x,y)
Returns mean squared error of fit of y data by MonitorGamma function of x. The
MonitorGamma parameters are x0=p(1) and gamma=p(2). We constrain 0^2 x 0^2 1 and
gamma^3 0, and augment the error when they are out of bounds, so that minimization
will always settle on in-bound values.

Denis Pelli 5/26/96