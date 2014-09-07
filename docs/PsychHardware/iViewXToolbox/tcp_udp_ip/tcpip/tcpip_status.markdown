---
layout: mfile
title: tcpip_status
categories:
  - tcpip
encoding: UTF-8
---

status=tcpip\_status(fid) Return a status value for tcpip connection.

Mainly usefull when you whant to detect that a connection is broken.
(return value 0)

# Possible status values:

TCPIP\_NOCONNECT   0 Not connected. Perhaps it has been broken. [Close](/docs/Close) it!
TCPIP\_SERVSOCKET  1   Server socket waiting for connections.
TCPIP\_STDIO       5   Connected to file (not implemented)
TCPIP\_CLIENT      10  Connected as client. Used tcpip\_open.
TCPIP\_SERVER      12  Connected as server  Used tcpip\_servopen or tcpip\_listen