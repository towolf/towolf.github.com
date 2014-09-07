---
layout: mfile
title: udp_plotter_demo
categories:
  - tcp_udp_ip
encoding: UTF-8
---

UDP\_PLOTTER\_DEMO - Opens a figure and starts to listen for UDP packages to plot.
Syntax:
  UDP\_PLOTTER\_DEMO
or
  UDP\_PLOTTER\_DEMO localport

This script is a demo that listen for a UDP packet (default port 3333) and
uses PLOT to dplay the sequence of doubles in the packet.

(C) 2002 Peter Rydesaeter