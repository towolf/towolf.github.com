---
layout: mfile
title: PhotopigmentQuantalEfficiency
categories:
  - PsychColorimetricData
encoding: UTF-8
---

 quantalEfficiencies = PhotopigmentQuantalEfficiency.(receptorTypes,[species],[source])

 Return estimate of the fraction of absorbed quanta that lead to an isomerization.

 Supported types:
   Any

 Supported species:
        Any.

 Supported sources:
    Generic (Default).
   None (returns 1 for all photoreceptor types)

 The generic source returns the value 0.667 for any species or type.  This
 is currently the only interesting source implemented.  The value comes from
 Rodieck RW, The First Steps in Seeing, page 472.

 7/25/03  dhb  Wrote it.
 8/9/13   dhb  Add type of 1.