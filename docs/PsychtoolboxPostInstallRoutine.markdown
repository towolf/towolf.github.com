---
layout: mfile
title: PsychtoolboxPostInstallRoutine
categories:
  - .
encoding: UTF-8
---

PsychtoolboxPostInstallRoutine(isUpdate [, flavor])  

Psychtoolbox post installation routine. You should not call this  
function directly! This routine is called by DownloadPsychtoolbox,  
or UpdatePsychtoolbox after a successfull download/update of  
Psychtoolbox. The routine performs tasks that are common to  
downloads and updates, so they can share their code/implementation.  

As PsychtoolboxPostInstallRoutine itself is downloaded or updated,  
it can contain code specific to each Psychtoolbox revision/release  
to perform special setup procedures for new features, to announce  
important info to the user, whatever...  

# Currently the routine performs the following tasks:  

1\. Clean up the Matlab/Octave path to Psychtoolbox: Remove unneeded .svn subfolders.  
2\. Contact the Psychtoolbox server to perform online registration of this  
   working copy of Psychtoolbox.  
3\. Add the PsychJava subfolder to the static Matlab class-path if neccessary.  
   This enables the Java-based GetChar support on Matlab.  
4\. Add the PsychStartup.m routine to Matlab's startup.m file on Windows.  
5\. Perform post-installation checks and basic troubleshooting.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychtoolboxPostInstallRoutine.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychtoolboxPostInstallRoutine.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychtoolboxPostInstallRoutine.m</code>
</div>
