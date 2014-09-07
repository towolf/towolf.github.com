---
layout: mfile
title: PR650init
categories:
  - PR650Toolbox
encoding: UTF-8
---

retval = PR650init(portNumber, [enableHandshaking])

Initialize serial port for talking to colorimeter.
Returns whatever character is sent by colorimeter

'enableHandshaking' allows you to enable handshaking.  By default,
handshaking is disabled.  To enable handshaking, set this value to 1 or
true.

11/26/07    mpr   added timeout if nothing is returned within 10 seconds.

In my experience, calling this function directly leads to poor performance
(usually no communication is ever established).  You should find the function
CMCheckInit in the PsychHardware folder, one folder up the tree from this one
(which is presumably PR650Toolbox).  Calling this function from CMCheckInit
should provide more reliable establishment of contact and hints on what to
try if contact fails.  -- MPR