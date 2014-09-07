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



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/iViewXToolbox/tcp_udp_ip/pnet_putvar.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/iViewXToolbox/tcp_udp_ip/pnet_putvar.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/iViewXToolbox/tcp_udp_ip/pnet_putvar.m</code>
</div>
