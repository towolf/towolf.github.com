---
layout: mfile
title: Rush
categories:
  - PsychPriority
encoding: UTF-8
---

[Rush](/docs/Rush)(rushedCode, priorityLevel)

Note: This function is not needed anymore. Use [Priority](/docs/Priority)() instead to
simplify your life. The function is only left for backward compatibility
to keep old code running.

[Rush](/docs/Rush) runs a critical bit of your Matlab code with minimal interruption by
other tasks. The first argument is a string containing Matlab code to be
passed to EVAL. Within the string, you can have multiple statements
separated by ";" or ",".

The optional "priorityLevel" argument specifies how much to block
interrupt tasks. Use MaxPriority to determine the highest priority that
allows normal operation of the functions you use, e.g. SND and SCREEN
'WaitBlanking'. We suggest you always call MaxPriority rather than hard
coding any particular priorityLevel, so that your program will gracefully
adapt to run optimally on any computer. Here's a typical use:

    [Screen](/docs/Screen)('Screens');  % Make sure all functions (SCREEN.mex) are in memory.
    i=0;                % Allocate all variables.
    loop={
        'for i=1:100;'
            '[Screen](/docs/Screen)(window,''WaitBlanking'');'
            '[Screen](/docs/Screen)(''CopyWindow'',w(i),window);'
        'end;'
    };
    priorityLevel=MaxPriority(window,'WaitBlanking');
    [Rush](/docs/Rush)(loop,priorityLevel);

Allowable 'priorityLevel' settings are described in "help [Priority](/docs/Priority)".

see also: [Priority](/docs/Priority)