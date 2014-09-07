---
layout: mfile
title: udp_send_demo
categories:
  - tcp_udp_ip
encoding: UTF-8
---

UDP\_SEND\_DEMO - a demo that sends a squence of doubles in network byte order to local or remote host

Syntax:
  UDP\_SEND\_DEMO
or
  UDP\_SEND\_DEMO function\_string
or
  UDP\_SEND\_DEMO function\_string hostname
or
  UDP\_SEND\_DEMO function\_string hostname portnumber

Default values:
   function\_string  is by default sin(0:0.1:6) that will be evaluated and transmitted
                    as a sequence of network byte ordered doubles (or generated datatype)

   hostname         is by default localhost but can be any hostname if you whant to send
                    the packet to an other host.

   portnumber       is by default 3333.


The purpose of this demo is to illustrate how a udp packat can be created, filled with numbers
and then transmitted to any host and udp port. Use this demo together with udp\_plotter\_demo
that receives and plott the packets of numbers.

# Example:

udp\_send\_demo sin(0:0.1:50)./(0:0.1:50) plotterhost 33333
