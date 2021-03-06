---
layout: mfile
title: ConfirmInfo
categories:
  - Utilities
encoding: UTF-8
---

 Syntax: [FigureHandle] = ConfirmInfo(TheQuestion,[ButtonString],[TimeoutPeriod])

 Purpose: Create simple dialog box asking user to verify receipt of information

 History: 1/11/05       mpr     modified this from TwoStateQuery
                     1/21/05        mpr     allowed font size to be reduced for longer strings
           5/3/06    mpr   added third argument to limit time for response;
                           defaults to Inf; works only in version 7 (requires
                           timer object class)
                     5/15/06        mpr     allowed figure to be non-modal; under that
                           condition, clicking button deletes figure; to make
                           nonmodal, in version 5, pass non-zero non-Inf third
                           argument; in version 7, pass NaN as third argument;
                           also added return argument to allow calling function
                           to delete figure if user fails to delete figure and
                           program proceeds
          8/26/06    mpr   repainted buttons in version 7
         12/14/07    mpr   commented call to RepaintAllPushButtons because
                           the Matlab bug is now almost fixed
         12/29/07    mpr   made three-line questions possible
                     1/3/08         mpr     introduced NLChar for cross-platform compatibility
          3/5/08     mpr   small cosmetic fix for new case where a third line
                           was needed even though Extent(3) \< 2...
          3/21/08    mpr   allowed return value to signal if user closed window
                           instead of clicking uicontrol button (works only if
                           figure is modal)
          3/31/08    mpr   added check to make sure search for appropriate
                           space does not overrun number of spaces
          5/20/13    mk Add text only fallback for Octave and non-GUI.