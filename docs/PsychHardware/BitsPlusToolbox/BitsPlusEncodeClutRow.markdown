---
layout: mfile
title: BitsPlusEncodeClutRow
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

bitsPlusClutRow = BitsPlusEncodeClutRow(theClut)

This is for the Cambridge Research Systems BITS++ 14-bit video DAC.
BitsPlusEncodeClutRow accepts the desired content for the CLUT (color
look up table) and encodes it so that it may be poked into the first (or
last) line of the image. The BITS++ will detect the "unlock" code and
transfer the CLUT data into the 256 entry, 3 channel, 14-bit CLUT.
<http://www.crsltd.com/>