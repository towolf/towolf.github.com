---
layout: mfile
title: PR655measspd
categories:
  - PR655Toolbox
encoding: UTF-8
---

[spd,qual] = PR655measspd(S,[syncMode])

Make a measurement of the spectrum.

01/16/09    tbc   Adapted from PR650Toolbox for use with PR655
10/26/10    dhb   Handle sync failure a little better.
3/8/11      dhb  Pass syncMode option to speed things up for displays where it doesn't work.