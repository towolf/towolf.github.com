---
layout: mfile
title: wintabfastLoop
categories:
  - WinTab
encoding: UTF-8
---

 function fastLoop

 Opens a PTB [Screen](/docs/Screen), attaches a tablet to the associated screen pointer wPtr and dumps out the contents of an event queue.


 pkt = WinTabMex(5) reads the latest data point out of a tablet's event queue. This queue is a buffer that can hold around 50 data points.
 This queue begins filling up after a call to WinTabMex(2), which empties the queue, and can be used to record movement data during
 stimulus presentation in a 'fast loop' (see fastLoop.m).

 pkt is a 8x1 column vector

 tabletTestData.mat:
           xPos                = pkt(1), x axis position (tablet coordinates)
           yPos                = pkt(2), y axis position (tablet coordinates)
           zPos                = pkt(3), z axis position (tablet coordinates)
           buttonState         = pkt(4), encoded button state (works a little erratically)
           serialNumber        = pkt(5)
           tabletTimeStamp     = pkt(6), time in ms from the tablet
           penStatus           = pkt(7), signals various events (eg penOutOfRange)
           penChange           = pkt(8), flags what has changed since the last sample

pkt(1:6) are straightforward, pkt(7:8) need some work on figuring out what it all means

Andrew D. Wilson, 2009 (adwkiwi@gmail.com)