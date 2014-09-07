---
layout: mfile
title: FORPCheck
categories:
  - FORP
encoding: UTF-8
---

FORPCheck Checks if a button of a FORP device (HH-5-CYL) is pressed.

# Usage:

   [KeyPressed,EventTime] = FORPCheck()


Return the key name (KeyPressed) of the pressed button and the
time (EventTime) of the status check.


   KeyPressed          Key name of the Pressed Button, empty string
                       if none pressed.


   EventTime           Time of keypress check, as returned by GetSecs.

# IMPORTANT NOTE:


   See FORPWait.

   Going through each device can be very time consuming. If would advise
   to unplug each unnecessary device, so less devices has to be checked.
   If you have got any advice for a better way to solve those problems, feel
   free to let me know:

          Florian Stendel
          Visual Processing Lab
          Universitaets - Augenklinik Magdeburg
          Leipziger Strasse 44
          \39120 Magdeburg
          Tel:    0049 (0)391 67 21723
          Email:  vincentdhs@gmx.de


   \10/10/06   fs   Wrote it.
   \10/16/06   mk   Add caching of device index.
   \10/17/06   fs   Done some restructuring and testing.
   \02/08/07   mk   New vendor id 6171 added to valid device lists.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychHardware/FORP/FORPCheck.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychHardware/FORP/FORPCheck.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychHardware/FORP/FORPCheck.m</code>
</div>
