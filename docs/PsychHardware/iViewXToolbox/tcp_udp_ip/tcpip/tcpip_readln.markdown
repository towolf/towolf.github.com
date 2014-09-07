---
layout: mfile
title: tcpip_readln
categories:
  - tcpip
encoding: UTF-8
---

[str,ok]=tcpip\_readln(fid,len)

fid   is file id.
len   is maximum length to be read.

Reads a line of charters terminated by newline character (LF).
If the a full line (until LF) isn available at the
moment a empty string will be returned.
CR and LF characters will not be returned in the string.

Returns ok set to 1 if a complete line whas recived.
