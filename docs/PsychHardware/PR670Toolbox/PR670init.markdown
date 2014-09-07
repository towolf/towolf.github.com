---
layout: mfile
title: PR670init
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670init - Initialize the serial port to talk to the PR-670.  

Syntax:  
retval = PR670init  
retval = PR670init(portNumber)  

Description:  
Initializes the serial port for talking to colorimeter. Returns whatever  
character is sent by colorimeter  

Input:  
portNumber (1xN char) - Name of the serial port to use.  

Output:  
retval (1xN char) - Character data returned from the PR-670.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/PR670Toolbox/PR670init.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/PR670Toolbox/PR670init.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/PR670Toolbox/PR670init.m</code>
</div>
