---
layout: mfile
title: mogldouble
categories:
  - wrap
encoding: UTF-8
---

--- OBSOLETE --- OBSOLETE --- OBSOLETE --- OBSOLETE ---
PSYCHTOOLBOX SPECIFIC double() implementation:

retval = mogldouble(arg) -- convert into
a double precision floating point number.

This routine takes an 'arg' of arbitrary
numeric class and converts it into an equivalent
object of double precision floating point format.

If a builtin double() function is available,
as on Matlab and Octave 3.2+, it calls the builtin
double() function.

Otherwise (Octave) it would call our own special
implementation.

This is no longer needed as of Octave 3.2.0, but we leave the function
here as many internal and external code relies on its presence.

# For Octave pre 3.2, this applied:

This is a hack needed to make OpenGL (MOGL) work
on GNU/Octave, despite Octave's lack of a single
precision data type.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/wrap/mogldouble.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/wrap/mogldouble.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/wrap/mogldouble.m</code>
</div>
