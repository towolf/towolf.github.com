---
layout: mfile
title: tcpip_viewbuff
categories:
  - tcpip
encoding: UTF-8
---

str=tcpip\_viewbuff(fid,len)

fid   file id for connection.
len   Maximum length of returned string.
str   Returned string as char.


Returns what's in incomming buffert but it will not
remove data from the buffert. A following tcpip\_read()
will return the same string.