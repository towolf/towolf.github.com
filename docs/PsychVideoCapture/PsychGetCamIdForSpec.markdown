---
layout: mfile
title: PsychGetCamIdForSpec
categories:
  - PsychVideoCapture
encoding: UTF-8
---

Return deviceIndex of a specified camera, one that matches given criteria.  

[deviceIndex, dev] = PsychGetCamIdForSpec([className][, inputNameOrPort][, instance][, engineId]);  

Searches for video sources which match given criteria. A handle to the  
first source that satisfies the criteria is returned in argument  
'deviceIndex' - You can open a connection to the source via  
[Screen](/docs/Screen)('OpenVideoCapture', windowPtr, deviceIndex, ...);  

The 2nd optional return argument contains the complete 'dev'ice  
description struct, as returned by [Screen](/docs/Screen)().  

Returns empty variables if no match can be made.  

# Optional criteria:  

'className' Index or name of video input device class: Default is to  
accept any class. This matches against the 'ClassName' property of the  
list returned by [Screen](/docs/Screen)('VideoCaptureDevices').  

'inputNameOrPort' selects the i'th input device of a matching class if an  
index is given (zero-based), or a specific named device, e.g., 'iSight'  
for the builtin iSight camera of Apple hardware.  

'instance' If multiple devices match, take the i'th device where i ==  
instance. By default, the first device (instance == 0) is assigned.  

'engineId' Enumerate for video capture engine 'engineId'. By default, the  
default videocapture engine is used.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychVideoCapture/PsychGetCamIdForSpec.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychVideoCapture/PsychGetCamIdForSpec.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychVideoCapture/PsychGetCamIdForSpec.m</code>
</div>
