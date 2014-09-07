---
layout: mfile
title: GetGITInfo
categories:
  - PsychOneliners
encoding: UTF-8
---

 gitInfo = GetGITInfo(directory)  

 Description:  
 Retrieves the git information on a specified directory or file.  This is  
 essentially a wrapper around the shell command "git".  

 Input:  
 directory (string) - Directory name of interest.  

 Output:  
 gitInfo (struct) - Structure containing the following information:  
   Path  
   Describe  
    Revision  
   LastCommit  
   RemoteRepository  
   RemoteBranch  
   LocalBranch  

 'gitInfo' will be empty if there is no git info for directory or if directory  
 does not exist.  

 7/11/13  dhb  Wrote it based on GetSVNInfo  
 7/12/13  dhb  More info, based on Ben Heasly's version of this in RenderToolbox3.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/GetGITInfo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/GetGITInfo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/GetGITInfo.m</code>
</div>
