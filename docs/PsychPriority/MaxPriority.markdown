---
layout: mfile
title: MaxPriority
categories:
  - PsychPriority
encoding: UTF-8
---

priorityLevel=MaxPriority([windowPtrOrScreenNumber],['WaitBlanking'],['PeekBlanking'],...  
                            ['BlankingInterrupt'],['SetClut'],['ClutMovie'],...  
                            ['SND'],['sound'],['speak'],...  
                            ['GetSecs'],['WaitSecs'],['cputime'],...  
                            ['KbCheck'],['KbWait'],['CharAvail'],['GetChar'],...  
                            ['EventAvail'],['GetClicks'],['GetMouse'],['GetTicks'])  

MaxPriority.m receives a list of one or more function names, in any  
order, and returns the maximum priorityLevel that will allow all the  
named functions to work normally on this computer. Use MaxPriority  
before calling RUSH, to select the highest priorityLevel that's  
compatible with all the functions that you're rushing.  

The name matching ignores case.  

# OS X  

On OS X all priority levels are safe for all functions. MaxPriority  
always returns 9, the highest priority level.  

To preserve compatibility with other platforms we recommend using  
MaxPriority in your script on OS X, instead of the constant 9.  

# WINDOWS  

[Priority](/docs/Priority) levels returned by MaxPriority are 0, 1 and 2.  
Although use of priority levels \> 1 is possible and allowed by MaxPriority  
if you don't try to acquire input from keyboard or mouse, it is discouraged  
to use levels \> 1 as this can interfere with execution of a lot of  
important system processes and severely reduce the stability of  
Windows execution.  

# LINUX  

MaxPriority always returns 1, although levels of up to 99 are possible.  
We recommend to sticking to the lowest level, unless some tweaking for a  
specific setup or situation is necessary.  
----  

See RUSH, [Priority](/docs/Priority), MovieDemo, ScreenTest, SCREEN [Preference](/docs/Preference) MaxPriorityForBlankingInterrupt,  
SCREEN [Preference](/docs/Preference) SetClutPunchesBlankingClock.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychPriority/MaxPriority.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychPriority/MaxPriority.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychPriority/MaxPriority.m</code>
</div>
