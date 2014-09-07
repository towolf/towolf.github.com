---
layout: mfile
title: MovieDemo
categories:
  - PsychDemos
encoding: UTF-8
---

MovieDemo  

Show a movie, easy as pie.  

The comments below review the difference between the OS 9 version of  
the toolbox and PTB-3.  

# New and different on OS Psychtoolbox:  

 The OS 9 Psychtoolbox is based on QuickTime and PTB-3 is  
 based on OpenGL.  Differences between these underlying graphics libraries  
 have unavoidably resulted in differences between the OS 9 and PTB-3  
 versions of [Screen](/docs/Screen); Some subfunctions of OS 9 [Screen](/docs/Screen) are replaced by  
 similar, but not identical functions in PTB-3.  

 In OS 9:                   In PTB-3  

  WaitBlanking              [Flip](/docs/Flip)  
  PutImage                  MakeTexture  
  CopyWindow                DrawTexture  

 WaitVBL vs. [Flip](/docs/Flip)  

  In OS 9 an onscreen window consisted of only one buffer: the front  
  buffer.  Any pixel drawn to an onscreen window would automatically  
  appear on the display as soon as the monitor scan passed  that pixel,  
  the maximum delay between drawing a pixel and its appearnce on the  
  monitor being one frame period.  To  prevent vertical shearing of  
  animated displays, Psyhctoolbox scripts called WaitBlanking before  
  updating the display.  WaitBlanking synchonrized drawing into vide RAM  
  wih the monitor scan by delaying the onset of drawing until the scan  
  reached the bottom right corener of the display, at which point a  
  vertical blank would occur while the CRT beam retraced to the upper  
  left corner of the display.  

  In contrast, PTB-3 onscreen windows by default have not one but two  
  buffers:  the front buffer and the back buffer.  In double-buffered  
  mode, all [Screen](/docs/Screen) drawing commands are issued to the back buffer, where  
  what is drawn is hidden from view.  The contents of the back buffer  
  remain hidden from view until The [Screen](/docs/Screen)('[Flip](/docs/Flip)', ...) command is  
  issued. [Flip](/docs/Flip) waits  until the vertical retrace and then interchages the  
  contents of the front and back buffers, bringining into view on the  
  display what had previosly been hidden in the back buffer.  

 OpenOffscrenWindow + PutImage + CopyWindow vs. MakeTexture + DrawTexture  

  In OS 9, PutImage copied a MATLAB matrix into an offsceen window.  The  
  offscreen Window could then be quickly copied to the display during an  
  animation.  Thus  PutImage was one part of three for quickly  
  displaying MATLAB matrices during an animation:  

      Steps to quickly display an image matrix in OS 9:  
        1\. Create an offscreen window by calling OpenOffscreenWindow  
        2\. Copy the matrix to an offsceen window using PutImage  
        3\. Copy the offscreen window to an onscreen window using  
        CopyWindow  

  Instead of using Offscreen Windows to quickly display MATLAB Matrices  
  the OSX Psychtoolbox uses Textures.  

      Steps to quickly display an image matrix in PTB-3:  
        1\. Create a texture and copy into it a matrix by using MakeTexture  
        2\. Copy the texture quickly to the onscreen window using  
        DrawTexure  

  What is the difference betwen offscreen windows and textures? The  
  difference is that Drawing commands such as FillOval may be  issued to  
  offscreen windows but not to Textures; You may only fill textures by  
  using matrices.  

  How do we draw ovals during an animation if we can not store them  
  within offscren or textures? Unlike QuickDraw, OpenGL is fast enought  
  to render all drawing commands directly to the display during an  
  animation loop. Except for MATLAB matrices stored in textures, there  
  should be no need to prerender and buffer what is displayed during  
  animation.  

 Animation loops: OS 9 VS PTB-3  

  To understand the differences between OS 9 and PTB-3 [Screen](/docs/Screen) its helpful  
  to compare animation loops:  

#   OS 9:  

      %create and fill offscreen windows here...  
      for i=1:numberOfMovieFrames  
          [Screen](/docs/Screen)(window, 'WaitBlanking');  
          [Screen](/docs/Screen)('CopyWindow', offscreenWindow(i), window);  
      end  

#   PTB-3:  

      %generate textures here...  
      for i=1:numberOfMovieFrames  
          [Screen](/docs/Screen)('DrawTexture', texture(i), window);  
          [Screen](/docs/Screen)(window, '[Flip](/docs/Flip)');  
      end  


See also: DriftDemo, PsychDemos.  


# HISTORY  

7/3/04   awi  Wrote it.  Based on Denis Pelli's MovieDemo for OS 9.  
7/19/04  awi  restored [Priority](/docs/Priority), and time tests, added option to plot results.  
7/24/04  awi  Cosmetic  
9/8/04   awi  Added Try/Catch.  
4/23/05  mk   Added [Priority](/docs/Priority)(0) to Catch-Section.  
11/19/06 dhb  Remove OSX from name.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/MovieDemo.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/MovieDemo.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/MovieDemo.m</code>
</div>
