---
layout: mfile
title: ConcatenationBug
categories:
  - PsychMatlabTests
encoding: UTF-8
---

Mathworks Case ID:  84454, reported 7/17/98  

Square and curly braces sometimes can't embrace multiple lines.  

# This works:  

{'a'  
'b'}  

# So does this:  

x={'a'  
'b'}  

# And this:  

x=char({'a'  
'b'})  

# But this fails:  

char({'a'  
'b'})  
??? 'b'}  
       |  
Missing operator, comma, or semi-colon.  


Shouldn't the braces work consistently?  

Case ID:  84454  

Denis,  

I am writing in response to your email of July 20, 1998, regarding the  
error you receive when pass CHAR an expression enclosed in curly braces.  

This has been verified here at The MathWorks, and it has been forwarded to  
our development staff to be addressed in a future release.  

...  

Sincerely,  

Vincent Hodges  
Technical Support Engineer  
vhodges@mathworks.com  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychMatlabTests/ConcatenationBug.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychMatlabTests/ConcatenationBug.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychMatlabTests/ConcatenationBug.m</code>
</div>
