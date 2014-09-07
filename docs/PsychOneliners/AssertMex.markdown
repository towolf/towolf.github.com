---
layout: mfile
title: AssertMex
categories:
  - PsychOneliners
encoding: UTF-8
---

Handle missing or dysfunctional MEX files on Matlab or Octave.  

AssertMex(targetname)  

AssertMex detects missing mex files.  Calling AssertMex from  
your help file, e.g. foo.m, asserts the existence of a mex file foo.mex.  
If no such mex file exists then AssertMex will exit with an error.  

Assert Mex is useful for detecting the error condition when a .m help  
file is mistakenly executed because the correspondig .mex file is  
missing. When foo.mex is missing, MATLAB silently executes the help file  
foo.m instead.  Calling AssertMex within foo.m detects and reports that  
error. E.g., in [Screen](/docs/Screen).m you'll find AssertMex('[Screen](/docs/Screen).m') to handle  
missing or dysfunctional [Screen](/docs/Screen) mex files properly.  
----  

See also: AssertOpenGL, COMPUTER, IsOSX, IsWin  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/AssertMex.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/AssertMex.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/AssertMex.m</code>
</div>
