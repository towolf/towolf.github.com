---
layout: mfile
title: pnet_putvar
categories:
  - tcp_udp_ip
encoding: UTF-8
---

PNET\_PUTVAR - Send matlab variable(s) of any type over PNET connection.

# Syntax:

  pnet\_putvar(con,variable1,variable2.....)

  Sends matlab variables over a TCP connection. The variablea must
  be recived with PNET\_GETVAR. Can also be used with UDP packets
  if the variable/variables fits inside an UDP packet.

Se also:  PNET\_GETVAR, PNET, PNET\_REMOTE
