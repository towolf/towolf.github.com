---
layout: mfile
title: pnet_getvar
categories:
  - tcp_udp_ip
encoding: UTF-8
---

PNET\_GETVAR - Gets any matlab variable (number-, cell-, struct- or object -array) from pnet.

# Syntax:

  [variable1, variable2,.....]=pnet\_getvar(con)

  Receives matlab variables over a TCP connection that was sent with
  PNET\_PUTVAR. This variable transfer uses its own non standard protocol.
  Can also be used with UDP packets if the variable/variables fits inside
  an UDP packet.

Se also:  PNET\_PUTVAR, PNET, PNET\_REMOTE
