---
layout: mfile
title: tcpip_servopen
categories:
  - tcpip
encoding: UTF-8
---

TCPIP\_SERVOPEN opens a blocking TCPIP server socket.

#  Call with:

   fid = tcpip\_servopen(port)

#  where:

   port   is the port number of the socket you wish to open.

   fid      is the retuned handle to the socket, if successful,
            -1 if unsuccessful.

 This function is obsolete.  It has been replaced with TCPIP\_SERVSOCKET
 and TCPIP\_LISTEN.  It is only included for backward compatibility.

 TCPIP\_SERVOPEN opens a TCPIP server socket with the requested PORT
 number.  This function blocks (waits) until a client socket has
 established a connection before returning FID.

#  EXAMPLE:

    disp('Waiting for someone to connect to port 4444...');
    fid = tcpip\_servopen(4444);
    if fid = -1
      error('TCP/IP Connection error!');
    end
    disp('Connection! :-)');
    disp('Now sending a message and closing!')
    tcpip\_write('Hello!!',string(10)); %string(10) generates newline
    tcpip\_close(fid);

 See also:  TCPIP\_SERVSPCKET, TCPIP\_LISTEN, TCPIP\_OPEN
            TCPIP\_CLOSE
