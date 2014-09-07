---
layout: mfile
title: tcpip_getfile
categories:
  - tcpip
encoding: UTF-8
---


 ret = tcpip\_getfile(ip\_fid,name)

 ip\_fid    file id for tcpip channel.
 name      Name of file to save as.
 ret       Return value.

Get a file over network with tcpip.
Using a own protocol for this system.
se tcpip\_sendfile()