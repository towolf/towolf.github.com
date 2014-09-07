---
layout: mfile
title: read_rle_rgbe
categories:
  - PsychContributed
encoding: UTF-8
---

read\_rle\_rgbe

Written by Lawrence A. Taplin (taplin@cis.rit.edu)

Based loosely on the c-code RGBE implementation written by Bruce Walters
http://www.graphics.cornell.edu/~bjw/rgbe.html

function to read a run length encoded RGBE picture file and header. This does
not work if the image is not RLE!!!

Note to Psychtoolbox users: Please use the higher level HDRRead.m
routine for better generality in your code. This routine is used as
helper for HDRRead.
