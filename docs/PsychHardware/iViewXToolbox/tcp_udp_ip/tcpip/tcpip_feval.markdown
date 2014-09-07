---
layout: mfile
title: tcpip_feval
categories:
  - tcpip
encoding: UTF-8
---

tcpip\_feval(ip\_fid,no\_ret\_args,'fun\_name',arg1,arg2,...) remote "feval"
Sends to server request to execute 'fun\_name' with argument....
no\_ret\_args specifies number of return arguments. If return arguments is
more then 0 then use tcpip\_feval\_end to get them later.
