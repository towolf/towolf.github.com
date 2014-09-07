---
layout: mfile
title: LumToRadiance
categories:
  - PsychColorimetric
encoding: UTF-8
---

 [radiance, radianceS] =...
    LumToRadiance(relativeSpectrum, relativeSpectrumS, luminance, [photopic])

 Convert luminance in photopic cd/m2 to radiance, given relative spectrum
 of the source.

 Variable photopic can take on values:
        'Photopic' (Default)
   'JuddVos'
   'Scotopic'

 7/29/03   dhb  Wrote it.