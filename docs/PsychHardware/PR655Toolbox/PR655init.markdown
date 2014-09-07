---
layout: mfile
title: PR655init
categories:
  - PR655Toolbox
encoding: UTF-8
---

retval = PR655init(portNumber, [enableHandshaking])

Initialize serial port for talking to colorimeter.
Returns whatever character is sent by colorimeter

Per PhotoResearch, handshaking is disabled.

11/26/07    mpr   added timeout if nothing is returned within 10 seconds.
01/16/09    tbc   Adapted from PR650Toolbox for use with PR655

It seems the iterative CMCheckInit method of initialization is not
necessary with the PR655, so one run of this seems to do the trick.
"usbmodem\*" seems to cover every instance I've run into. Not sure about
the prevalance of using usbmodem as a generic identifier, but if you can
afford the PR655, you're probably on some more respectable form of internet
connection. -TBC
