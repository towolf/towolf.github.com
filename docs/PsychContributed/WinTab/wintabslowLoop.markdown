---
layout: mfile
title: wintabslowLoop
categories:
  - WinTab
encoding: UTF-8
---

 function slowLoop\(samplingRate\)

 Opens a PTB [Screen](/docs/Screen), attaches a tablet to the associated screen pointer wPtr and records data from a graphics tablet. The data is sorted
 and output to a .mat file and an Excel file.

#  INPUTS:
 samplingRate: sampling rate in Hz for your tablet. Establish this using fastLoop.m

 pkt = WinTabMex\(5\) reads the latest data point out of a tablet's event queue. This queue is a buffer that can hold around 50 data points.
 This queue begins filling up after a call to WinTabMex\(2\), which empties the queue, and can be used to record movement data during
 stimulus presentation in a 'fast loop' \(see fastLoop.m\).

 pkt is a 8x1 column vector

 tabletTestData.mat:
           xPos                = pkt\(1\), x axis position \(tablet coordinates\)
           yPos                = pkt\(2\), y axis position \(tablet coordinates\)
           zPos                = pkt\(3\), z axis position \(tablet coordinates\)
           buttonState         = pkt\(4\), encoded button state \(works a little erratically\)
           serialNumber        = pkt\(5\), an index of which data point this is since the last call to WinTabMex\(2\)
           tabletTimeStamp     = pkt\(6\), time in ms from the tablet
           penStatus           = pkt\(7\), signals various events \(eg penOutOfRange\)
           penChange           = pkt\(8\), flags what has changed since the last sample
           getsecTimeStamp     = the time at which the data was collected from the start of the trial, using PTB's GetSecs function
           pktData             = matrix of data, compiled into columns for writing to Excel

pkt\(1:6\) are straightforward, pkt\(7:8\) need some work on figuring out what it all means

Andrew D. Wilson, 2009 \(adwkiwi@gmail.com\)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychContributed/WinTab/wintabslowLoop.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychContributed/WinTab/wintabslowLoop.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychContributed/WinTab/wintabslowLoop.m</code>
</div>
