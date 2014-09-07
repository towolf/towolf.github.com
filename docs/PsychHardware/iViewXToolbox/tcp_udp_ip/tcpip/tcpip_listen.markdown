---
layout: mfile
title: tcpip_listen
categories:
  - tcpip
encoding: UTF-8
---

TCPIP\_LISTEN(socket) - Listning for connetions on open socket.
Socket must first be opened with TCPIP\_SERVSOCKET, both sockets
and connections are closed with TCPIP\_CLOSE().

This frunction returns a hander to connection if ther is one
waiting, else it returns -1.