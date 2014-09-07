---
layout: mfile
title: Bandpass
categories:
  - PsychSignal
encoding: UTF-8
---

w=[Bandpass](/docs/Bandpass)(n,fLow,fHigh) returns a 1xn window, a band-pass filter. The
elements represent gain at each freq, uniformly spaced from -1 to 1 of
Nyquist frequency. fLow and fHigh are the positive cut-off frequencies
on this scale. We pass frequencies in the interval [fLow,fHigh). The
asymmetric use of bounds guarantees that complementary filters will add
to 1: [Bandpass](/docs/Bandpass)(n,0,f)+[Bandpass](/docs/Bandpass)(n,f,Inf)==ones(1,n). If fHigh is omitted
it's assumed to be Inf. Also see Bandpass2.