---
layout: mfile
title: FindSerialPort
categories:
  - PsychHardware
encoding: UTF-8
---

Syntax: PortNumber = FindSerialPort\(\[PortString\]\[, forIOPort=0\]\[, dontFail=0\]\)

Purpose: Find serial port number/name associated with a particular input string.

If the optional parameter 'PortString' is omitted, the routine will use a
built-in list of default serial port names to search for. Otherwise it
will try to find a serial port with a name matching 'PortString'.

If the optional flag 'forIOPort' is zero or left out, the routine will return
a 'PortNumber' compatible with use of the SerialComm\(\) serial port driver
for MacOS/X with Matlab. If 'forIOPort' is non-zero, it will return a
serial port device string in 'PortNumber', suitable for use with the new
[IOPort](/docs/IOPort) serial port driver which works on all operating systems and
runtime environments.

By default, the function will abort with an error message if it doesn't
find a matching useable port, or if it finds multiple matches, ie. if the
mapping is ambiguous. If you set the optional flag 'dontFail' to 1, it
will continue in such cases without any error message: It will simply
return an empty \[\] PortNumber if no matching port can be found, or the
1st detected matching port, if multiple matches exist.

Please note that support of SerialComm for OS/X is a legacy, only left
for backwards compatibility\! New code should only use the new [IOPort](/docs/IOPort)
driver and therefore set the 'forIOPort' flag to 1.

For intersting in-depths comments on the use of this function with PR-650
style photometers, read the source code of this file.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/FindSerialPort.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/FindSerialPort.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/FindSerialPort.m</code>
</div>
