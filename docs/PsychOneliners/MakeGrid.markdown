---
layout: mfile
title: MakeGrid
categories:
  - PsychOneliners
encoding: UTF-8
---

[raster] = MakeGrid(nrow,ncol,xres,yres,plxres,plyres)

Makes raster of elements centered on screen / in image (leftover space is
divided equally over the edges)

input:
  ncol:   number of columns
  nrow:   number of rows
  xres:   horizontal resolution of screen or image
  yres:   vertical resolution of screen or element
  plxres: hor resolution of raster element (can be smaller than xres, not larger)
  plyres: vert resolution of raster element (can be smaller than yres, not
          larger)

output
  raster: struct with boundaries of raster elements
          is a matrix of structs of size number of raster elements
          vertically X number of raster element horizontally

IH    2008
DN    2008 v1.1 - coordinates sometimes faulty
DN    2008 v1.2 - coordinates sometimes faulty (actually solved this
                  time) + input checking