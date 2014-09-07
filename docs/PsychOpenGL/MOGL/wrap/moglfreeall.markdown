---
layout: mfile
title: moglfreeall
categories:
  - wrap
encoding: UTF-8
---

moglfreeall -- Free all memory buffers inside mogl which were previously  
created via calls to ptr = moglmalloc(...) or ptr = moglcalloc(...).  

After successfull release, all Pointers will be invalid, \*do not use them anymore\*  
or Matlab/Octave will possibly crash or do other nasty things!  

moglcalloc()'ed or moglmalloc()'ed memory buffers can be released as well  
one by one via moglfree(), and they are automatically released when  
moglcore is clear'ed via clear moglcore, clear mex or clear all.  



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/moglfreeall.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/moglfreeall.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/moglfreeall.m</code>
</div>
