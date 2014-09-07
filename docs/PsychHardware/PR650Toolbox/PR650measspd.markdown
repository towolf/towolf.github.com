---
layout: mfile
title: PR650measspd
categories:
  - PR650Toolbox
encoding: UTF-8
---

[spd,qual] = PR650measspd(S,[syncMode])

Make a measurement of the spectrum.  Tries to be smart
about using sync or not, unless it is turned off by
passed variable.

syncMode = 'on':  Try to sync integration time with display.  Retry without if it fails. (default)
syncMode = 'off': Don't try to sync.

8/26/10  dhb  Add DEBUG option to figure out why this dies sometimes.
3/8/11   dhb  Pass syncMode option to speed things up for displays where it doesn't work.