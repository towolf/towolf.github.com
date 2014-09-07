---
layout: mfile
title: ComputeRMSE
categories:
  - PsychGamma
encoding: UTF-8
---

rmse = ComputeRMSE(data,predict,SUPRESS\_WARNING)

Compute a root fractional SSE between data and prediction.
Inputs should be column vectors.

The routine badly named, because what it computes
is not what anyone would call an RMSE.  A better
name for the routine would be ComptueFSSE or something
like that.

Indeed, it now calls through an appropriately named
ComputeFSSE, and issues an annoying warning encouraging
the user to change the calling form.

2/3/96   dhb  Added improved comments.
1/13/13  dhb  Added cautionary comment about what this routine does.
              as well as message that would tell an unsuspecting user
              at runtime.
         dhb  Added mechanism to suppress the warning message.